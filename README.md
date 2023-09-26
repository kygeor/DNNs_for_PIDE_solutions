# DNNs_for_PIDE_solutions
Jupyter notebooks containing the development, training and testing of Deep Neural Network models for the solutions of parabolic PIDEs

The following scripts are based on the DNN construction as described and built in the github by J. Blechschmidt, O. G. Ernst ("Three Ways to Solve Partial Differential Equations with Neural Networks - A Review"). We have used simulation-based DNN training to extend these method to solve Partial Integro-Differential Equations (PIDEs) that arise from various underlying stochastic models and applications. The specific forms of the models from which the corresponding PIDEs follow can be found in the corresponding paper (https://arxiv.org/abs/2309.12384) and/or the thesis (https://www.researchgate.net/publication/374158001_Discrete_continuous_and_machine_learning_models_with_applications_in_credit_risk).

**1. DNN_1D_PIDE.ipynb**
   - Simulations of the underlying jump Ornstein-Uhlenbeck process for training the DNN
   - Construction of the DNN achitecture with 2 inputs, initial position and time until maturity
   - Training the DNN, with output the PD function Psi(x, t)
   - Additional graphs and plots of the resulting function

**2. DNN_RS_PIDE.ipynb**
   - Simulations of the underlying regime switching jump Ornstein-Uhlenbeck process for training the DNN. The switching process is modelled with a Continuous Time Markov Chain (CTMC)
   - Construction of the DNN achitecture with 3 inputs, initial position, time until maturity and the initial regime
   - Training the DNN, with output the PD function Psi(x, t, rho)
   - Additional graphs and plots of the resulting function 

**3. DNN_SV_PIDE.ipynb**
   - Simulations of the underlying stochastic volatility jump Ornstein-Uhlenbeck process for training the DNN. The stochastic volatility model is modelled using a CIR stochastic differential equation and the resulting asset process follows a Heston-type model
   - Construction of the DNN achitecture with 3 inputs, initial position, time unitl maturiy and the initial volatility 
   - Training the DNN, with output the PD function Psi(x, t, y)
   - Additional graphs and plots of the resulting function
     
**4. DNN_Generalize_PIDE.ipynb**
   - Simulations of the underlying generalized jump Ornstein-Uhlenbeck process for training the DNN. The generalized model combines both the regime switching and stochastic volatility models to construt a general case of asset value model
   - Construction of the DNN achitecture with 4 inputs, initial position, time unitl maturiy, initial regime and the initial volatility 
   - Training the DNN, with output the PD function Psi(x, t, rho, y)
   - Additional graphs and plots of the resulting function
   (- The DNN is able to solve the PIDE that results from this model, whereas the Finite Difference scheme fails due to the "curse of dimensionality")  

**5. DNN_family_of_PIDEs.ipynb**
   - Simulations of a one dimensional continuous Ornstein-Uhlenbeck process
   - Simulations of a one dimensional jump continuous Ornstein-Uhlenbeck process
   - Construction of the DNN achitecture with 4 inputs now representing the initial position and the parameters of the OU process 
   - Training the DNN, with output the PD function Psi(x, kappa, theta, sigma), hence the model has "learnt" the PD function for a large family of stochastic processes 
   - Additional graphs and plots of the resulting function(s)
