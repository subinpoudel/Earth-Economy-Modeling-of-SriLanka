# Earth-Economy-Modeling-of-SriLanka
Country: Sri Lanka

## Discription
This is the final assignment of APEC 8601- Natural Resources Course. In this project, I use tools like GTAP-InVEST earth economy modeling to estimate the economic value of various ecosystem services to the Sri Lankan economy. I will also compute the global-local estimates of the influence of ecosystem services on the computable general equilibrium.

### Step 1
The first step involves creating a new copy of run_test_standard.py for Sri Lanka inside the seals folder.  This step involves changing line 24, and changing the project name to "test_lanka". The country alpha_code "Aoi code" for Sri Lanka is LKA. The scenarios under baseline are set to SSP2 under exogenous_level.  For the purpose of our analysis, I use two additional scenarios namely SSP1 and SSP5. For the years I insert 2030, 2035, and 2040 under "years" for the SSP1 and SSP5 while keeping the baseline year at 2017.

The next step is to run the defined SSP scenarios. To run the new SSP scenarios, first download the correct/specific coarse_projections_input_path from Land Use Harmonization data. Save this data in the base_data under the lulh2 folder approriately or using a consistent directory structure from the baseline input data. Package "hazelbean" is used to run parallel processing. It creates separate project folders given the name given in line 24. we created a new project under the specific name "test_lanka.py" to run this. 

Now after running everything in the debugger console, I have a new set of scenario definitions that I can use in the test_lanka.py. You can examine this file as scenario_defininitions1a.csv. To examine the results, you can now look in the seals folder under projects and you should find the LULC maps (and other output) in a folder called lanka_standard alongside the initial folder for the initial test run called test_standard. The script is run in earth_economy_devstack and a previously defined Python kernel.

You will want to put the scenario_definitions.csv file into a new project folder labeled test_lanka\input before running the test_lanka.py. If you do not, then it will populate the standard test run with observations and shapefiles of Rwanda instead of the new country that you are interested in (Sri Lanka). 

### Plot these seven LULC maps and scenarios.
#### LULC 2017 with Baseline (SSP2)

![lulc_esa_seals7_luh2-message_2017](https://github.com/subinpoudel/Earth-Economy-Modeling-of-SriLanka/assets/141669397/9f1fa809-5a25-45b9-a2b6-e3e05587ca84)


#### LULC 2030 with SSP1 and RCP26

![lulc_esa_seals7_ssp1_rcp26_luh2-message_bau_2030](https://github.com/subinpoudel/Earth-Economy-Modeling-of-SriLanka/assets/141669397/031297b5-fa79-4ce1-875c-733584043633)

#### LULC 2035 with SSP1 and RCP26

![lulc_esa_seals7_ssp1_rcp26_luh2-message_bau_2035](https://github.com/subinpoudel/Earth-Economy-Modeling-of-SriLanka/assets/141669397/4c8bd915-061d-497d-be94-87e2d6c8dbec)



#### LULC 2040 with SSP1 and RCP26

![lulc_esa_seals7_ssp1_rcp26_luh2-message_bau_2040](https://github.com/subinpoudel/Earth-Economy-Modeling-of-SriLanka/assets/141669397/f8501722-ec44-4adf-b6c2-2dd011e17276)



#### LULC 2030 with SSP5 and RCP85

![lulc_esa_seals7_ssp5_rcp85_luh2-message_bau_2030](https://github.com/subinpoudel/Earth-Economy-Modeling-of-SriLanka/assets/141669397/222940df-b61b-46ca-97a6-3357af835e1a)



#### LULC 2035 with SSP5 and RCP85

![lulc_esa_seals7_ssp5_rcp85_luh2-message_bau_2035](https://github.com/subinpoudel/Earth-Economy-Modeling-of-SriLanka/assets/141669397/926f2426-c8d3-4068-9bab-6c9e6785de31)

#### LULC 2040 with SSP5 and RCP85
![lulc_esa_seals7_ssp5_rcp85_luh2-message_bau_2040](https://github.com/subinpoudel/Earth-Economy-Modeling-of-SriLanka/assets/141669397/36f0a770-7680-46b3-86a5-dbd98d9f4cec)

## Adding a new "policy" layer 
Making it consistent with other friends in the group, I implemented the policy that any protected area can be converted to any land use type. To implement this policy, I change the "strict_pa" coefficients under the default_global_coefficients.csv from 0 to 1. Then I run the code under new coefficients again. The change observed under different scenarios defined earlier under the new policy layer is shown below. 

