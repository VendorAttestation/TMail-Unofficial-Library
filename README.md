# TMail-Unofficial-Library

# Usage

```
//init client
TMail client = new TMailClient("https://urltmail.url", "APIKEY HERE");
 
 //gen new email GenerateEmail(int length)
var email = await client.GenerateEmail(8);
 
//check
var emails = await client.CheckEmail(email); // Will return Waiting until emails arrive.
while (await client.CheckEmail(email) == "Waiting.")
{
	await Task.Delay(1000);
}

Console.WriteLine(emails);
```

# Install via Nuget
```cs
Install-Package TMail.API
```

