# Get Report Message with SMS Connexion

Retrieves a single message report from SMS Connexion.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/single/:msgId`
- **Base URL:** `https://api.sms.cx`
- **Official documentation:** [Get Report Message](https://sms.cx/sms-api-documentation/#operation/GetSingleReport)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `msgId` | path | `string` | yes | Message UUID. |
