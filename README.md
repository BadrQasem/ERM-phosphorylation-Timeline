# ERM-phosphorylation-Timeline
ERM protein phosphorylation timeline and adipocyte differentiation from different literatures
import matplotlib.pyplot as plt
import numpy as np

# Simulated time points (in days)
days = np.array([0, 2, 4, 6, 8, 10, 12])

# Simulated expression levels (relative units: arbitrary)
rhoa_rock = [1.0, 0.4, 0.3, 0.5, 0.6, 0.6, 0.6]
pparg =     [0.1, 0.3, 0.6, 0.8, 1.0, 1.0, 0.9]
fabp4 =     [0.0, 0.2, 0.5, 0.8, 1.0, 1.0, 0.9]
cebpb =     [1.0, 0.8, 0.4, 0.2, 0.1, 0.0, 0.0]
ucp1 =      [0.1, 0.1, 0.2, 0.4, 0.7, 1.0, 1.0]  # thermogenic marker

# Plotting
plt.figure(figsize=(10, 6))
plt.plot(days, rhoa_rock, label='RhoA/ROCK1/2', color='red', linewidth=2)
plt.plot(days, pparg, label='PPARγ', color='blue', linewidth=2)
plt.plot(days, fabp4, label='FABP4', color='green', linewidth=2)
plt.plot(days, cebpb, label='C/EBPβ', color='orange', linestyle='--', linewidth=2)
plt.plot(days, ucp1, label='UCP1 (thermogenesis)', color='purple', linestyle='-.', linewidth=2)

plt.title("Gene Expression Dynamics in Adipogenesis", fontsize=14)
plt.xlabel("Days of Differentiation", fontsize=12)
plt.ylabel("Relative Expression (AU)", fontsize=12)
plt.legend()
plt.grid(True)
plt.tight_layout()
plt.show()
