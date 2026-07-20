# Import Subscribers with Sendloop

## Endpoint

- **Method:** `POST`
- **Path:** `/subscriber.import/json`
- **Base URL:** `https://{subdomain}.sendloop.com/api/v3`
- **Official documentation:** [Import Subscribers](https://chmyos.notion.site/Import-Subscribers-eb12e964eb804901a180f084a2c77c0c)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ListID` | body | `number` | yes | ID of the target list to import subscribers |
| `Subscribers[0][EmailAddress]` | body | `string` | yes | First subscriber email address |
