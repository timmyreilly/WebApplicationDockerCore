# Docker ASP.NET Core Sample: 

## Run Locally:
`$ docker run -it -d -p 85:80 timmyreilly/aspnetcoresample ` 

## Ron on Azure Linux Web Apps 
Image:
timmyreilly/aspnetcoresample

Run:
`docker run -p 80:80 timmyreilly/aspnetcoresample `

## Build Docker Image after changes: 
`docker build .\bin\Debug\netcoreapp1.0\publish\ -t timmyreilly/aspnetcoresample:latest `

## Push Changes: 
`docker push timmyreilly/aspnetcoresample:latest ` 


# Sample Workflow: 

Clone the Repo 

Build the Project

Make a Change 

Publish the change 
`$ dotnet publish `

Rebuild the image: 
`$ docker build .\bin\Debug\netcoreapp1.0\publish\ -t timmyreilly/aspnetcoresample:latest `

List the images just to make sure its there: 
`$ docker images`

Run it: 
`$ docker run -it -d -p 81:80 timmyreilly/aspnetcoresample:latest `

See that its running:
`$ docker ps`

Push the changes: 
`$ docker push timmyreilly/aspnetcoresample:latest ` 

Make sure Azure is pointing to the right tag! 

### Supporting slides: 
https://doc.co/oVusK4 

### References: 
- Builds on: https://hub.docker.com/r/microsoft/aspnetcore/ 
- [Helpful guide from Scott Hanselman](http://www.hanselman.com/blog/ExploringASPNETCoreWithDockerInBothLinuxAndWindowsContainers.aspx)
- [Helpful video from App Services Team](https://channel9.msdn.com/Events/Connect/2016/199) 