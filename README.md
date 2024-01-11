**Explanation**
1. Begin by downloading pgAdmin from (https://www.pgadmin.org/download/)
2. Proceed to download PostgreSQL from (https://www.postgresql.org/download/)
        -During installation, click "Next" and set a secure password of your choice
4. Download the Visual Studio Community (https://visualstudio.microsoft.com/downloads/)
        -Launch pgAdmin and navigate to the "Servers" tab
   
   <img width="960" alt="Untitled1" src="https://github.com/marijaspasova00/C-ExapleRepo_Marija/assets/119892747/a79fc8c5-b0d8-4787-9698-0028c3d4e717">
   
        -Enter the password you specified during the PostgreSQL installation
6. Copy the repository from (https://github.com/evolutionary-architecture/evolutionary-architecture-by-example/tree/main) then clone the repository in Visual Studio
        -Open Visual Studio and choose "Clone Repository" or download the repository as a zip file
   
  <img width="960" alt="Untitled" src="https://github.com/marijaspasova00/C-ExapleRepo_Marija/assets/119892747/8917810e-4685-467b-ac5b-8b8e842b898a">
  
        -Open the project bearing the name Chapter-1-initial-architecture
   7. Access the "appsettings.Development.json" file.
      
  <img width="960" alt="Untitled2" src="https://github.com/marijaspasova00/C-ExapleRepo_Marija/assets/119892747/8cfba917-8bdc-47e0-a760-c9ef01a0b00e">
  
        -Modify the following section:
   From:
      
   "ConnectionStrings": {
   "Passes": "Host=postgres:5432;Database=fitnet;Username=postgres;Password=mysecretpassword",
   "Contracts": "Host=postgres:5432;Database=fitnet;Username=postgres;Password=mysecretpassword",
   "Reports": "Host=postgres:5432;Database=fitnet;Username=postgres;Password=mysecretpassword",
   "Offers": "Host=postgres:5432;Database=fitnet;Username=postgres;Password=mysecretpassword"

 }
 
   To:
 
  "AllowedHosts": "*",
  "ConnectionStrings": {
  "Passes": "Host=localhost:5432;Database=fitnet;Username=postgres;Password=postgres",
  "Contracts": "Host=localhost:5432;Database=fitnet;Username=postgres;Password=postgres",
  "Reports": "Host=localhost:5432;Database=fitnet;Username=postgres;Password=postgres",
  "Offers": "Host=localhost:5432;Database=fitnet;Username=postgres;Password=postgres"
}

-Update "Host" to use "localhost," replace "mysecretpassword" in the "Password" field with the password you set during PostgreSQL installation, and add "AllowedHosts": "*".

8. Launch the application. This modification ensures the correct connection to the PostgreSQL database

<img width="960" alt="Untitled3" src="https://github.com/marijaspasova00/C-ExapleRepo_Marija/assets/119892747/d8c19e71-4069-4c2e-80ea-e39affd7d969">

10. Verify the presence of the "Fitnet" database in PostgreSQL.

 <img width="960" alt="Untitled4" src="https://github.com/marijaspasova00/C-ExapleRepo_Marija/assets/119892747/b613cab8-2ec4-4625-a6f8-3f728aef23f7">

