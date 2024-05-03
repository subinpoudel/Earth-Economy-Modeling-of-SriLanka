# Earth-Economy-Modeling-of-SriLanka
Country: Sri Lanka

## Discription
This is the final assignment of APEC 8601- Natural Resources Course. In this project, I use tools like GTAP-InVEST earth economy modeling to estimate the economic value of various ecosystem services to the Sri Lankan economy. I will also compute the global-local estimates of the influence of ecosystem services on the computable general equilibrium.

### Step 1
The first step involves creating a new copy of run_test_standard.py for Sri Lanka inside the seals folder.  This step involves changing line 24, and changing the project name to "test_lanka". The country alpha_code "Aoi code" for Sri Lanka is LKA. The scenarios under baseline are set to SSP2 under exogenous_level.  For the purpose of our analysis, I use two additional scenarios namely SSP1 and SSP5. For the years I insert 2030, 2035, and 2040 under "years" for the SSP1 and SSP5 while keeping the baseline year at 2017.

The next step is to run the defined SSP scenarios. To run the new SSP scenarios, first download the correct/specific coarse_projections_input_path from Land Use Harmonization data. Save this data in the base_data under the lulh2 folder approriately or using a consistent directory structure from the baseline input data. Package "hazelbean" is used to run parallel processing. It creates separate project folders given the name given in line 24. we created a new project under the specific name "test_lanka.py" to run this. 

Now after running everything in the debugger console, I have a new set of scenario definitions that I can use in the test_lanka.py. You can examine this file as scenario_defininitions1a.csv. To examine the results, you can now look in the seals folder under projects and you should find the LULC maps (and other output) in a folder called lanka_standard alongside the initial folder for the initial test run called test_standard. The script is run in earth_economy_devstack and a previously defined Python kernel.

You will want to put the scenario_definitions.csv file into a new project folder labeled test_lanka\input before running the test_lanka.py. If you do not, then it will populate the standard test run with observations and shapefiles of Rawanda instead of the new country that you are interested in (Sri Lanka). 

### Plot these seven LULC maps and scenarios.
#### LULC 2017 with Baseline (SSP2)

