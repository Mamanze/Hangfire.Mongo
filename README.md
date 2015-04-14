Hangfire.Raven
==============


RavenDB support for [Hangfire](http://hangfire.io/) library. By using this library you can store all jobs information in RavenDB.

# Usage

```csharp
app.UseHangfire(config =>
{
	config.UseRavenStorage("<connection string>", "<database name>");
});
```

For example:

```csharp
app.UseHangfire(config =>
{
	config.UseRavenStorage("mongodb://localhost", "ApplicationDatabase");
});
```

## Custom collections prefix

To use custom prefix for collections names specify it on Hangfire setup:

```csharp
app.UseHangfire(config =>
{
	config.UseRavenStorage("mongodb://localhost", "ApplicationDatabase",
  	  	new RavenStorageOptions { Prefix = "custom" } );
});
```

License
-------

Hangfire.Raven is released under the [MIT License](https://raw.githubusercontent.com/sergun/Hangfire.Mongo/master/LICENSE).
