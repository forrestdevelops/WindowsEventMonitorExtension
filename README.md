
# Windows Event Message Monitor extension

Windows Event message Monitor works with .NET Agent Extension Manager to capture and report specific windows event and the message associated with it.


## Requirement

- .NET Agent Extension Manager 
- The AppDynamics .NET Agent 
- .NET 4.0 or later


## Artifacts

- [extension.xml](/publish/2.2.0/extension.xml) 
- [WindowsEventMonitor.dll ](/publish/2.2.0/WindowsEventMonitor.dll)


### Installation

![alt text](/readme_images/FolderStructure.png)

- Download and unzip the artifacts in the [publish directory](/publish/)
- copy extension.xml and WindowsEventMonitor.dll from the publish folder to a new dirctory: 
`<Extension Manager Root Directory>/Extensions`


### Configure exstenstion
- Edit extension.xml to provide controller details and target specific events.

- Provide controller user credentials. These are required for publishing custom events to the controller. For single-tenant controllers, use "customer1" for the account. Controller host/port are read from the Agent Configuration file (config.xml).

```xml
  <controller-info user="username" account="customer1" password="password" />
```



## Changes in 2.2.0

This extenstion differs from the [original](https://github.com/Appdynamics/WindowsEventMonitorExtension) as it enables the message an addional property to filter by for the custom event 


## How to use 

Assure that the extenstion is running and enabled in the .Net extenstion monitor
![alt text](/readme_images/Extenstion.png)

In the custom eents filter apply the desired filter to your custom event type and click "Apply"
![alt text](/readme_images/usage.png)

