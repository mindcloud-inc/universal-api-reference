# Submit an appeal for account blocking with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/fraud/appeal`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Submit an appeal for account blocking](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reason` | body | `string` | yes | Reason for appealing the account blocking |
