## Biotechnical Energy Efficiency Function (B.E.E.F.)
### The energy-efficiency fungal plastic degradation model
Welcome to our model for calculating optimal conditions for efficient plastic degradation through fungi. Troughout this model, the word incubation time will be used frequently. This refers to the time (in days) it takes to fully degrade a batch of plastic. This model has been created as part of a research for the course Project 4 at the University of Amsterdam. All the scientifical justification for this model can be found there.

### The model consists of different functions that roughly perform the following tasks:
 - **Data Processing:** Converts user-provided CSV files into Python lists.
 - **Fitting:** Fits the data to Gaussian, inverse and linear models and returns their formulas for further calculations.
 - **Equalization:** Adjusts functions for temperature and particle size for accurate model output.
 - **Incubation Time calculations** Calculates the total incubation time for different combinations of temperature and particle size and saves these in a dataframe.
 - **Energy Calculation:** Calculates total energy consumption for combinations of temperature and particle size from the dataframe and adds constant energy costs from the user inputs.
 - **Efficiency Calculation:** Determines energy efficiency by dividing degradation rate by energy cost from the dataframe.
 - **Plotting:** Creates an interactive plot that shows the relationship between energy cost and incubation time, along with the optimal parameters and the efficiency.

For running this model, some fungi-specific data is required. The following user inputs have to be acquired as csv files:
  - a matrix for temperature (°C) against incubation time (days)
  - a matrix for particle size (mm³) against incubation time (days)
  - a matrix with the energy cost (J/mg) for shredding to certain particle sizes (mm³)

Besides this there are also other constants and data that are required for running this model:
  - the size of your bioreactor (m³)
  - the plastic concentration in your bioreactor (mg/mL)
  - the temperature your bioreactor reaches while running after stabilizing its temperature and the wattage this requires. Give this as: 'wattage, temperature reached'
  - the energy cost for potentially running the UV radiation machine (W)
  - potential time dependent extra energy costs that do not fit in another category (W)
  - potential time independent extra energy costs that do not fit in another category (J)

### Running the model
After giving all these datapoints and constants, the model is capable of running the rest of the calculations. To run the entire model, run each of the code parts in order. After running the last code part, the model will ask for the user inputs. If you've given these correctly, the model will start calculating. It will first give intermediary outputs in the form of a plot with the gaussian and inverse fit for temperature and particle size respectivelly and a pandas DataFrame with all the calculated points. The final output will be an interactive bokeh plot showing the relationship between energy cost (MwH) and incubation time (days). The user can hover over every individual point of the plot to see the optimal parameters (temperature and particle size) and the efficiency (degradation rate / energy).

## Notes

 -  The model assumes that all questions are in the context of the Google Colab environment or Jupyter Notebooks.
 - For detailed information on each function, please refer to the comments within the code.
 - The first code block where google drive is imported is not possible in Jupyter Notebook. It is only necessary for accessing your data, which can also be uploaded manually.
 - The plot can be created using both mplcursors and bokeh depending on the environment in which the code is run. The code uses bokeh in case of google colab and mplcursors in all other cases.
