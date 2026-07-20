# Update Session with CoachAccountable

Updates a session in CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Update Session](https://www.coachaccountable.com/APIDocs#Session.update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `SessionID` | body | `number` | yes | — |
| `title` | body | `string` | no | Maximum length: 200. |
| `dateOf` | body | `date` | no | — |
| `timeOf` | body | `string` | no | — |
| `content` | body | `string` | no | Maximum length: 100000. |
| `visibility` | body | `list` | no | Accepted values: `*`, `C`, `P`. |
