# Add Client File From URL with CoachAccountable

Adds a client file from a URL in CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Add Client File From URL](https://www.coachaccountable.com/APIDocs#ClientFile.addAsURL)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientID` | body | `number` | yes | The ID of the Client with whom to share this File. |
| `URL` | body | `string` | yes | The URL of the link to share Maximum length: 300. |
| `title` | body | `string` | no | Maximum length: 200. |
| `folder` | body | `string` | no | Maximum length: 500. |
| `description` | body | `string` | no | Maximum length: 1000. |
