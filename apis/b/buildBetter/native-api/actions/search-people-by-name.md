# Search People By Name with BuildBetter

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.buildbetter.app/v1`
- **Official documentation:** [Search People By Name](https://docs.buildbetter.ai/pages/CRM%20Integration/people-and-companies#finding-people)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `searchText` | body | `string` | yes | Find people whose first name, last name, or email matches this text. |
| `limit` | body | `number` | no | Maximum number of people to return. |
