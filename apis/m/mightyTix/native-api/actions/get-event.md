# Get Event with Mighty Tix

Retrieves an event from Mighty Tix.

## Endpoint

- **Method:** `POST`
- **Path:** `admin-api/graphql`
- **Base URL:** `https://mindcloudmttix260403.mightytix.com`
- **Official documentation:** [Get Event](https://mightytix.com/docs/admin-api#query-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.id` | body | `string` | yes | Event ID from the Mighty Tix Admin GraphQL docs. |
