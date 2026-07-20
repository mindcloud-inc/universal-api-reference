# Create Venue with Mighty Tix

Creates a new venue in Mighty Tix.

## Endpoint

- **Method:** `POST`
- **Path:** `admin-api/graphql`
- **Base URL:** `https://mindcloudmttix260403.mightytix.com`
- **Official documentation:** [Create Venue](https://mightytix.com/docs/admin-api#mutation-createOneVenue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input` | body | `object` | yes | CreateOneVenueInput object from the Mighty Tix Admin GraphQL docs. |
