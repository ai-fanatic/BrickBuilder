<img src="https://www.ashlingpartners.com/wp-content/uploads/2021/07/logo-ashling-partners.svg" width="300"/>

# Reusable Component Documentation
Standard documentation template used for Ashling Partner's reusable assets

## Basic Information
|                |                                          |
|----------------|------------------------------------------|
| Name           | [ComponentName]                     |
| Description    | [Component Description] |
| Language       | [Component Language]                            |
| Component Type | [Component Type]                                 |
| Category       | [Component Category]                              |
| Usage          | [Component Description] |

## Code Summary
### Studio Dependencies
| Name                      | Version |
|---------------------------|---------|
| [Dependency1 Name]  | Version# |
| [Dependency1 Name] | Version#   |

### Arguments
| Name                | Direction | Type      | Description                              |
|---------------------|-----------|-----------|------------------------------------------|
| in_ContinueOnError       | in        | Bool  | OPTIONAL- Default value is false which will result in any exception encountered being thrown back to invoking process. True will suppress any exception encountered and return control to invoking process          |
| in_CustomException       | in        | Exception  | OPTIONAL- Default value is nothing and will result in the specific exception encountered thrown. If exception argument is provided, any exception thrown from activity will be overriden by the exception argument provided          |
| out_Assertion      | out        | Bool  | REQUIRED: Boolean passed out of component library. If all component activities are executed without exception, TRUE will be passed out; otherwise FALSE will be passed. NOTE: 'out_Assertion' = FALSE boolean will only be useful if 'in_ContinueOnError' is set to TRUE; thus enabling control return WITHOUT throwing          |
| in_CustomTimeout       | in        | Int32  | OPTIONAL- If no value provided, the default 30,000 milliseconds (30 seconds) will be set as timeout for UI activities. If value provided, UI activitiy timeout(s) will be be overridden at the discretion of the developer          |


## Test Cases