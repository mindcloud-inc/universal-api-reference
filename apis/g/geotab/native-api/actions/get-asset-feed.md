# Get Asset Feed with Geotab

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://{server}/apiv1`
- **Official documentation:** [Get Asset Feed](https://developers.geotab.com/myGeotab/apiReference/methods/GetFeed/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fromVersion` | body | `string` | no | Last version returned by a previous feed call. Omit on the first call to obtain the current toVersion. |
| `resultsLimit` | body | `number` | no | Maximum number of Device changes to return, up to 5,000. |
| `propertySelector` | body | `object` | no | — |
