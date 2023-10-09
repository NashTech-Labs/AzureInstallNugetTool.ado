# AzureInstallNugetTool.ado
This template can be used to acquire a specific version of Nuget. Also, use this template to change the version of Nuget used in the Nuget tasks.

## Pipeline Requirements

The dotNet Module pipeline requires the following parameters to be defined:

Parameters:


| Name  | Displayname | type | Default | Values | Opional/Required | Comments |
| ------------- | ------------- | :-------------: | :-------------: | :-------------: | :-------------: | ------------- |
| NugetToolVersion | Version of NuGet.exe to install | String | | | Optional | A version or version range that specifies the NuGet version to make available on the path. Use x as a wildcard |
| checkLatest | Always check for new versions | Boolean | false | true / false | Optional | When this boolean is set to true, the task always checks for and downloads the latest available version of NuGet.exe that satisfies the version spec.  |

These parameters provide multiple use case options for the setvariables templates pipeline, enable/disable flags for the utilization of different templates as per the requirements.


## Use Cases

### Direct use of a template

You can directly call a particular template as per the requirement. for example: 

  ```yaml
  # azure-pipeline.yml
  resources:
  repositories:
    - repository: Template
      type: github
      name: your_username/AzureInstallNugetTool.ado
      ref: <respective branch name>
      endpoint: 'githubServiceConnectioNname'

  steps:
  # passing the parameters
  - template: 
        parameters:
          

        
  
Make sure to adjust the repository name, branch name, and parameter values according to your project's requirements.

  ```
