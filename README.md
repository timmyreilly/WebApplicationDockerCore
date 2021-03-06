# Docker ASP.NET Core Sample: 

### Prereqs: 
- [Visual Studio Community 2015](http://visualstudio.com/free) 
- [ASP.NET Core with .NET Core](https://www.microsoft.com/net) 
- [Docker for Windows](https://docs.docker.com/docker-for-windows/) 
- [Visual Studio Tools for Docker](http://aka.ms/DockerToolsForVS)


## Run Locally:
`$ docker run -it -d -p 85:80 timmyreilly/aspnetcoresample ` 

## Run on Azure Linux Web Apps 
Image:
timmyreilly/aspnetcoresample

Run:
`docker run -p 80:80 timmyreilly/aspnetcoresample `

----


# Sample Workflow for your own project: 

Clone the Repo 

Restore Nuget Packages 

Build the Project

Make a Change 

Got to root of project: `$ cd .\WebApplicationDockerCore\src\WebApplicationDockerCore\ ` 

Publish the change 
`$ dotnet publish `

Rebuild the image: 
`$ docker build .\bin\Debug\netcoreapp1.0\publish\ -t yourname/aspnetcoresample:latest `

List the images just to make sure its there: 
`$ docker images`

Run it: 
`$ docker run -it -d -p 81:80 yourname/aspnetcoresample:latest `

See that its running:
`$ docker ps`

Visit `http://localhost:81/ ` to see your site. 

Push the changes: 
`$ docker push yourname/aspnetcoresample:latest ` 


If you have it running on Azure make sure you use the right tag. i.e:  

<kbd>
<img src="http://i.imgur.com/BWNTwdx.png" width="500">
</kbd>

### Supporting slides: 
https://doc.co/oVusK4 

### References: 
- Builds on: https://hub.docker.com/r/microsoft/aspnetcore/ 
- [Helpful guide from Scott Hanselman](http://www.hanselman.com/blog/ExploringASPNETCoreWithDockerInBothLinuxAndWindowsContainers.aspx)
- [Helpful video from App Services Team](https://channel9.msdn.com/Events/Connect/2016/199) 