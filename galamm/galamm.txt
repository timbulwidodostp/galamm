# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Generalized additive mixed models with latent variables Use galamm With (In) R Software
install.packages("galamm")
library("galamm")
galamm = read.csv("https://raw.githubusercontent.com/timbulwidodostp/galamm/main/galamm/galamm.csv",sep = ";")
# Estimation Generalized additive mixed models with latent variables Use galamm With (In) R Software
galamm <- galamm(formula = y ~ x + (0 + loading | id), data = galamm, family = c(gaussian, binomial), 
family_mapping = ifelse(galamm$itemgroup == "a", 1L, 2L), load.var = "itemgroup", lambda = matrix(c(1, NA), ncol = 1), factor = "loading")
summary(galamm)
# Generalized additive mixed models with latent variables Use galamm With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished