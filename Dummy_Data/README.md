# README
## Dummy Data for B.E.E.F. Model
The basic premise of our model, is that the user uses their own data from biological experiments
as input for the model. Currently, there are no data available on the optimal functioning conditions
of different parameters for plastic-degrading fungi. But without this data, the model cannot be tested. 
So we created our own data to be able to test the model.

The data we created is based upon theoretical background and will follow the same mathematical relationships
as the real data would. We share our dummy data in this folder, so that others can also use this data to test
the B.E.E.F. model and help us improve it.

### The files we share are:
- dummy_temp_ct.csv: This is a csv file with different temperatures (°C) in the first column and their associated
  incubation time (days) in the second column. This file can be used for input directly and does not have to be edited anymore.
- dummy_part_size_ct.csv: This is a csv file with different particle sizes (mm³) in the first column and their associated
  incubation time (days) in the second column. This file can be used for input directly and does not have to be edited anymore.
- dummy_part_size_energy.csv: This is a csv file with different particle sizes (mm³) in the first column and their associated
  energy cost (J/mg) in the second column. This file can be used for input directly and does not have to be edited anymore.
  This data comes from research by Buckshumiyan et al. (2023).
- dummy_other_values.txt:  This is a text file that includes the other inputs of the dummy data that are needed to run the model.
The user must copy the values from the files themselves and input it into the model.

### References
Buckshumiyan, A., Babu, S., Prakash, M., & Arasu, G. (2023). Recycling of plastic wastage by die shredder machine. Materials Today Proceedings. https://doi.org/10.1016/j.matpr.2023.04.022 