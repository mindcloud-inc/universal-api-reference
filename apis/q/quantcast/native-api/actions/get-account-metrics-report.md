# Get Account Metrics Report with Quantcast

Retrieves an account metrics report from Quantcast.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/graphql`
- **Base URL:** `https://developers.quantcast.com`
- **Official documentation:** [Get Account Metrics Report](https://developers.quantcast.com/docs/graphql-api/reference/queries/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `number` | yes | Quantcast account ID to report on. |
| `startDate` | body | `string` | yes | Report start date in YYYY-MM-DD format. |
| `endDate` | body | `string` | yes | Report end date in YYYY-MM-DD format. |
| `timezone` | body | `string` | no | Timezone used to interpret the report range. |
| `breakdowns` | body | `string` | yes | Quantcast breakdown display name, for example Day. |
| `metrics` | body | `string` | yes | Quantcast metric display name, for example Impressions. |
