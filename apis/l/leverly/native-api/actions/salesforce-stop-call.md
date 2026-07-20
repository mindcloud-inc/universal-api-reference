# Salesforce Stop Call with Leverly

## Endpoint

- **Method:** `POST`
- **Path:** `/salesforce/unpark`
- **Base URL:** `https://app.leverly.com/main`
- **Official documentation:** [Salesforce Stop Call](https://leverly.com/kb/salesforce-stop-calls/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Id` | body | `string` | yes | Salesforce lead ID sent in the outbound message. |
| `Phone` | body | `string` | yes | Lead primary phone number. |
