# Create Event with Mighty Tix

Creates a new event in Mighty Tix.

## Endpoint

- **Method:** `POST`
- **Path:** `admin-api/graphql`
- **Base URL:** `https://mindcloudmttix260403.mightytix.com`
- **Official documentation:** [Create Event](https://mightytix.com/docs/admin-api#mutation-createOneEvent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input` | body | `object` | yes | CreateOneEventInput object from the Mighty Tix Admin GraphQL docs. |
