# CoronaVirus COVID-19 daily registered cases in each provinces/towns in Germany and Italy
This repository provides updated datasets in Python files (.npz binary files in NumPy format) containing historical case numbers of the spread of COVID-19 in each province/town in Germany and Italy.

# Example on how to read the data for a specific province
import numpy as np

loaded_data = np.load('italy/Bari.npz')  # or: loaded_data = np.load('germany/SK Hamburg.npz')

sorted(loaded_data.files)  # Output: ['date_of_registration', 'number_of_new_cases']

date_of_registration = loaded_data['date_of_registration']
number_of_new_cases = loaded_data['number_of_new_cases']

print(date_of_registration)
print(number_of_new_cases)
