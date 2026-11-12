# Get Visit with Jobber

## Endpoint

- **Method:** `POST`
- **Path:** `graphql`
- **Base URL:** `https://api.getjobber.com/api`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `visitId` | body | `string` | yes | The Jobber visit ID used to find its job. |
| `columns` | body | `string` | no | Select the Jobber visit fields to return. |
