# Docker ASP.NET Core Sample: 

##Run:
`$ docker run -it -d -p 85:80 timmyreilly/aspnetcoresample` 

##OR on Azure Linux Web Apps 
Image:
timmyreilly/aspnetcoresample

Run:
`docker run -p 80:80 timmyreilly/aspnetcoresample`

## Make Changes: 
`docker build .\bin\Debug\netcoreapp1.0\publish\ -t timmyreilly/aspnetcoresample:latest `

## Push Changes: 
`docker push timmyreilly/aspnetcoresample:latest` 