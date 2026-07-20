# Create Prospect with Klenty

Creates a prospect in Klenty.

## Endpoint

- **Method:** `POST`
- **Path:** `/prospects`
- **Base URL:** `https://api.klenty.com/apis/v1/user/{username}`
- **Official documentation:** [Create Prospect](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_17d72e781c)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Account` | body | `string` | no | Prospect account field value. |
| `City` | body | `string` | no | Prospect city. |
| `CompanyDomain` | body | `string` | no | Prospect company domain. |
| `CompanyEmail` | body | `string` | no | Company email address. |
| `CompanyPhone` | body | `string` | no | Company phone number. |
| `Country` | body | `string` | no | Prospect country. |
| `Department` | body | `string` | no | Prospect department. |
| `Email` | body | `string` | yes | Prospect email address. |
| `LinkedinURL` | body | `string` | no | Prospect LinkedIn URL. |
| `Location` | body | `string` | no | Prospect location. |
| `MiddleName` | body | `string` | no | Prospect middle name. |
| `Phone` | body | `string` | no | Prospect phone number. |
| `Title` | body | `string` | no | Prospect job title. |
| `TwitterId` | body | `string` | no | Prospect Twitter field value. |
| `FirstName` | body | `string` | no | Prospect first name. |
| `LastName` | body | `string` | no | Prospect last name. |
| `FullName` | body | `string` | no | Prospect full name. |
| `Company` | body | `string` | no | Prospect company name. |
| `List` | body | `string` | no | List name to add the prospect to. |
| `Tags` | body | `string` | no | Pipe-delimited tags to add to the prospect. |
| `CustomFields` | body | `list<object>` | no | Custom field key/value entries for the prospect. |
| `Owner` | body | `string` | no | Owner email address to assign. |
