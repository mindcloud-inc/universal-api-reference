# List People by Company with BuildBetter

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.buildbetter.app/v1`
- **Official documentation:** [List People by Company](https://docs.buildbetter.ai/pages/CRM%20Integration/people-and-companies#finding-people)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | body | `string` | yes | Return people linked to this company ID. |
| `limit` | body | `number` | no | Maximum number of people to return. |
