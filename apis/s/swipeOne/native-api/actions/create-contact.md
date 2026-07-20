# Create Contact with Swipe One

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces/:workspaceId/contacts`
- **Base URL:** `https://api.swipeone.com/api`
- **Official documentation:** [Create Contact](https://docs.swipeone.com/en/articles/10545314-contacts#h_18dd8b78d4)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `city` | body | `string` | no |
| `country` | body | `string` | no |
| `department` | body | `string` | no |
| `facebook` | body | `string` | no |
| `gender` | body | `string` | no |
| `industry` | body | `string` | no |
| `line1` | body | `string` | no |
| `line2` | body | `string` | no |
| `linkedin` | body | `string` | no |
| `occupation` | body | `string` | no |
| `state` | body | `string` | no |
| `timezone` | body | `string` | no |
| `twitter` | body | `string` | no |
| `website` | body | `string` | no |
| `workspaceId` | path | `string` | yes |
| `zipcode` | body | `string` | no |
| `firstName` | body | `string` | no |
| `lastName` | body | `string` | no |
| `fullName` | body | `string` | no |
| `email` | body | `string` | no |
| `phone` | body | `string` | no |
| `address` | body | `object` | no |
| `birthday` | body | `date` | no |
| `socialMediaUrls` | body | `object` | no |
| `teamSize` | body | `number` | no |
| `annualRevenue` | body | `number` | no |
