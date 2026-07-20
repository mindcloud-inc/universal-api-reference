# Get Project Live Insights with Microsoft Clarity

Retrieves project live insights from Microsoft Clarity.

## Endpoint

- **Method:** `GET`
- **Path:** `/export-data/api/v1/project-live-insights`
- **Base URL:** `https://www.clarity.ms`
- **Official documentation:** [Get Project Live Insights](https://learn.microsoft.com/en-us/clarity/setup-and-installation/clarity-data-export-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `numOfDays` | query | `number` | no | Number of days to export from the current time. Allowed values are 1, 2, or 3. |
| `dimension1` | query | `list<string>` | no | The first dimension used to break down insights. Allowed values are Browser, Device, Country/Region, OS, Source, Medium, Campaign, Channel, or URL. Accepted values: `Browser`, `Campaign`, `Channel`, `Country/Region`, `Device`, `Medium`, `OS`, `Source`, `URL`. |
| `dimension2` | query | `list<string>` | no | The second dimension used to break down insights. Allowed values are Browser, Device, Country/Region, OS, Source, Medium, Campaign, Channel, or URL. Accepted values: `Browser`, `Campaign`, `Channel`, `Country/Region`, `Device`, `Medium`, `OS`, `Source`, `URL`. |
| `dimension3` | query | `list<string>` | no | The third dimension used to break down insights. Allowed values are Browser, Device, Country/Region, OS, Source, Medium, Campaign, Channel, or URL. Accepted values: `Browser`, `Campaign`, `Channel`, `Country/Region`, `Device`, `Medium`, `OS`, `Source`, `URL`. |
