# Update Virtual Business Card with RICOH360 Tours

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://bbomwcm27nhalfwjvwzy6qbrim.appsync-api.us-west-2.amazonaws.com`
- **Official documentation:** [Update Virtual Business Card](https://help.ricoh360.com/hc/en-us/articles/11956798675603-Specifications-for-Brand-Banner-Business-Card-and-Tripod-Cover)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | query | `string` | no | Business-card style description content. |
| `tourId` | query | `string` | no | Tour ID to update business-card content for. |
| `tourName` | query | `string` | no | Tour name to keep on the updated tour. |
