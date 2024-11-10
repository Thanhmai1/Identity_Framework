<h1>Create project Identity Framework</h1>
<h3>Create project</h3>
- Download Library
<pre>
  <code>
    dotnet add package   
    Microsoft.AspNetCore.Identity.EntityFrameworkCore
    dotnet add package Microsoft.EntityFrameworkCore.InMemory
    dotnet add package Microsoft.EntityFrameworkCore.SqlServer
    dotnet add package Microsoft.EntityFrameworkCore.Tools
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
- Open 'Program.cs':
<pre>
  <code>
    builder.Services.AddDbContext<ApplicationDBContext>(options =>
            {
                var connectionsString = builder.Configuration.GetConnectionString("DefaultConnection");
                options.UseSqlServer(connectionsString);
            });
  </code>
</pre>
- Open terminal
<pre>
  <code>
    Add-Migration FirstMigration
    Updata-Database
  </code>
</pre>
