# Delete Venue with Mighty Tix

Deletes an existing venue from Mighty Tix.

## Endpoint

- **Method:** `POST`
- **Path:** `admin-api/graphql`
- **Base URL:** `https://mindcloudmttix260403.mightytix.com`
- **Official documentation:** [Delete Venue](https://mightytix.com/docs/admin-api#mutation-deleteOneVenue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input` | body | `object` | yes | DeleteOneVenueInput object from the Mighty Tix Admin GraphQL docs. |
