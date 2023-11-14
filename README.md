# General-linear-modelling-in-R-binomial-
# Simulated data with a binary response variable
set.seed(123)
data <- data.frame(
  Y = factor(sample(c("Success", "Failure"), 100, replace = TRUE)),
  X1 = rnorm(100),
  X2 = rnorm(100)
)

# Fit a logistic regression model (GLM with binomial family)
glm_model <- glm(Y ~ X1 + X2, data = data, family = binomial)

# Display a summary of the GLM
summary(glm_model)
