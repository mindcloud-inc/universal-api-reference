# Delete Event with Mighty Tix

Deletes an existing event from Mighty Tix.

## Endpoint

- **Method:** `POST`
- **Path:** `admin-api/graphql`
- **Base URL:** `https://mindcloudmttix260403.mightytix.com`
- **Official documentation:** [Delete Event](https://mightytix.com/docs/admin-api#mutation-deleteOneEvent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input` | body | `object` | yes | DeleteOneEventInput object from the Mighty Tix Admin GraphQL docs. |
