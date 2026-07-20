# Create Audience from LinkedIn URL with LaGrowthMachine

Creates an audience in LaGrowthMachine from a LinkedIn URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/audiences`
- **Base URL:** `https://apiv2.lagrowthmachine.com/flow`
- **Official documentation:** [Create Audience from LinkedIn URL](https://documenter.getpostman.com/view/2071164/TVCmSkH2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audience` | body | `string` | yes | Audience name to populate from the LinkedIn search or post. |
| `identityId` | body | `string` | yes | Identity ID used to impersonate the LinkedIn search query. |
| `linkedinPostCategory` | body | `string` | no | Post interaction category when importing from a LinkedIn post. |
| `linkedinUrl` | body | `string` | yes | LinkedIn regular search URL, Sales Navigator search URL, or LinkedIn post URL. |
