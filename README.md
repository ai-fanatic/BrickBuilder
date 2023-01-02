<img src="https://www.ashlingpartners.com/wp-content/uploads/2021/07/logo-ashling-partners.svg" width="300"/>

# Brick Builder Documentation
Standard documentation template used for Ashling Partner's reusable assets

## Basic Information
|                |                                          |
|----------------|------------------------------------------|
| Name           | BrickBuilder           |
| Description    | Rebuilds a Uipath Studio solution xamls into the Ashling Reusable Component Template |
| Language       | VB                            |
| Component Type | Stuido Project                                 |
| Category       | Util                              |
| Usage          | Attended Automation

## Features
* Organizes the reusable xamls from your Studio solution into individual UiPath projects solutions for Brick Bucket submission
* Creates Test files for the component
* Updates template avtivity titles, sequence names, etc.
* Merges project dependencies from source project
* Updates project.json with name and description
* Merges namepsaces from source xaml
* Merges arguments from source xamls
* Merges xaml body from source xaml into template Try/Catch scope
* Creates and populates README.md file


## Instructions
1. Place your UiPath solutions(s) in the BrickBuilder/Data/Output folder location
2. Run BrickBuilder via Studio or Assistant
3. Select Analyze
    * This will create Customize.xlsx in the Output path
    * The Customize.xlsx file lists all of the identified components.  
4. Update Customize.xlsx - Save and Close Excel
    * The NewActivityName, Category, and Description should be updated as needed.
    * The NewActivityName field must be unique.
5. Select Build
6. Check Output folder

## Post Build
* Review the Source_ActivityName.xaml file against the new activity xaml to ensure Build accuracy 
* Delete the Source_ActivityName.xaml
* Activity Test files will need to be completed and executed so that they get documented in the README.md file




## Code Summary

### Studio Dependencies
| Name                      | Version |
|---------------------------|---------|
| UiPath.Excel.Activities  | [2.11.4] |
| UiPath.System.Activities | [21.10.4]   |
| UiPath.Testing.Activities | [22.4.2]   |
| UiPath.WebAPI.Activities | [1.13.1] |

### Arguments
| Name                | Direction | Type      | Description                              |
|---------------------|-----------|-----------|------------------------------------------|
| in_OutputPath       | in        | String  | Path to a directory containing one or more UiPath Studio projects          |
| in_InputPath       | in        | String  |  Path where output will be written      |

### Config.xaml
| Name                | Value                  | Description                              |
|---------------------|------------------------|------------------------------------------|
| ExcludedFolders     | Framework,Tests        | These folders will be excluded from the Brick Builder process |
| ExcludedFiles       | Main.xaml,Process.xaml | These xaml files will be excluded |
| TestCaseCount       | 3                      | Number of test cases to create |


