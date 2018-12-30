# Powershell-Json
Powershell Json serializer and deserializer.
Works with all Powershell versions, no dependencies.
Works with Powershell objects of multiple depths (dicts of lists of dicts, etc).

# Convert from Json to Powershell object (for example Hashtable) :
$JsonString = Get-Content .\File.json -Encoding utf8

$MyObject = $JsonString | ConvertFrom-JSON

$MyObject.GetType().Name

# Convert from Powershell object to Json :
$JsonString = $MyObject | ConvertTo-JSON

Set-Content -Path .\File.json -Value $JsonString -Encoding utf8
