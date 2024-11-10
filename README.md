<h1>Create project Identity Framework</h1>
<h3>Create project</h3>
- Download Library
<pre>
  <code>
    Microsoft.AspNetCore.Identity.EntityFrameworkCore
    Microsoft.EntityFrameworkCore.InMemory // If you use Memory
    //If you use SQL Server
    Microsoft.EntityFrameworkCore.SqlServer
    Microsoft.EntityFrameworkCOre.Tools
  </code>
</pre>
- Create new folder "Data"
- Create new file name "ApplicationDBContext"
+ Create constructer for ApplicationDBContext
+ Add connecting string in 'appsettings.json'
<pre>
  <code>
    "ConnectionStrings": {
      "DefaultConnection": "Data Source={SERVER NAME};Initial   
      Catalog={DB NAME};Integrated Security=True;Trust Server
      Certificate=True"
    },
  </code>
</pre>
