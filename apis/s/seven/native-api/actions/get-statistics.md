# Get Statistics with Seven

Retrieves account statistics from Seven.

## Endpoint

- **Method:** `GET`
- **Path:** `/analytics`
- **Base URL:** `https://gateway.seven.io/api`
- **Official documentation:** [Get Statistics](https://docs.seven.io/en/rest-api/endpoints/account#statistics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | query | `date` | no | Start date of the statistics in the format YYYY-MM-DD. The date from 30 days ago is set by default. |
| `end` | query | `date` | no | End date of the statistics. The current day by default. |
| `label` | query | `string` | no | Only shows data for a specific label. |
| `subaccounts` | query | `number` | no | Receive data only for the main account, for all your (sub)accounts or only for specific subaccounts  ID of a subaccount - Displays the data of a specific subaccount.  all - Displays the data of all accounts and subaccounts cumulatively.  only_main - Displays only the data of the main account. |
| `group_by` | query | `date` | no | Defines the grouping of the data. The default value is date . |
