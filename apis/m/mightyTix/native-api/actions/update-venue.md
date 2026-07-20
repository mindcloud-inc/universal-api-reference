# Update Venue with Mighty Tix

Updates an existing venue in Mighty Tix.

## Endpoint

- **Method:** `POST`
- **Path:** `admin-api/graphql`
- **Base URL:** `https://mindcloudmttix260403.mightytix.com`
- **Official documentation:** [Update Venue](https://mightytix.com/docs/admin-api#mutation-updateOneVenue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input` | body | `object` | yes | UpdateOneVenueInput object from the Mighty Tix Admin GraphQL docs. |
