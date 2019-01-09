# GRS（整个项目代码）

# c-statistics（计算c-statistics）
Cstat(model)
# the confidence interval of c-statistics（计算c-statistics的置信区间）

# PredictABEL（calibration）
cOutcome <- 8
cNonGenPred1 <- c(2:3)
cNonGenPred2 <- c(2:3, 6)
cNonGenPred3 <- c(2:3, 6, 7)
cNonGenPred4 <- c(2:4, 6, 7)
cNonGenPred5 <- c(2:5, 6, 7)
cNonGenPredCat1 <- c(0)
cNonGenPredCat2 <- c(0)
cNonGenPredCat3 <- c(0)
cNonGenPredCat4 <- c(4)
cNonGenPredCat5 <- c(4)
cNonGenPred6 <- c(2:3)
cNonGenPred7 <- c(2:3, 6)
cNonGenPred8 <- c(2:3, 6, 7)
cNonGenPred9 <- c(2:4, 6, 7)
cNonGenPred10 <- c(2:5, 6, 7)
cNonGenPredCat6 <- c(0)
cNonGenPredCat7 <- c(0)
cNonGenPredCat8 <- c(0)
cNonGenPredCat9 <- c(4)
cNonGenPredCat10 <- c(4)
cGenPred1 <- c(0)
cGenPred2 <- c(0)
cGenPred3 <- c(0)
cGenPred4 <- c(0)
cGenPred5 <- c(0)
cGenPred6 <- c(10:14)
cGenPred7 <- c(10:14)
cGenPred8 <- c(10:14)
cGenPred9 <- c(10:14)
cGenPred10 <- c(10:14)
cGenPredsCat1 <- c(0)
cGenPredsCat2 <- c(0)
cGenPredsCat3 <- c(0)
cGenPredsCat4 <- c(0)
cGenPredsCat5 <- c(0)
cGenPredsCat6 <- c(0)
cGenPredsCat7 <- c(0)
cGenPredsCat8 <- c(0)
cGenPredsCat9 <- c(0)
cGenPredsCat10 <- c(0)
data <- as.data.frame(data)
riskmodel1 <- fitLogRegModel(data=data, cOutcome=cOutcome, cNonGenPreds=cNonGenPred1, cNonGenPredsCat=cNonGenPredCat1, cGenPreds=cGenPred1, cGenPredsCat=cGenPredsCat1)
ORunivariate(data=data, cOutcome=cOutcome, cGenPreds=cGenPred10, filenameGeno="GenoOR.txt", filenameAllele="AlleleOR.txt")
opar <- par(no.readonly = TRUE)
par(mfrow=c(2, 5))
predRisk1 <- predRisk(riskmodel1)
predRisk2 <- predRisk(riskmodel2)
predRisk3 <- predRisk(riskmodel3)
predRisk4 <- predRisk(riskmodel4)
predRisk5 <- predRisk(riskmodel5)
predRisk6 <- predRisk(riskmodel6)
predRisk7 <- predRisk(riskmodel7)
predRisk8 <- predRisk(riskmodel8)
predRisk9 <- predRisk(riskmodel9)
predRisk10 <- predRisk(riskmodel10)
rangeaxis <- c(0,1)
groups <- 10
plotCalibration(data=data, cOutcome=cOutcome, predRisk=predRisk1, groups=groups, rangeaxis=rangeaxis, plottitle = 'Model 1 (Without GRS)')
legend('topleft', legend = c('P for goodness of fit 0.679'), bty = 'n', cex = .6, inset = .01)




































