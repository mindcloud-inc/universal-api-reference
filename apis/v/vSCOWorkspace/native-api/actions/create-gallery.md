# Create Gallery with VSCO Workspace

Creates a new gallery in VSCO Workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/gallery`
- **Base URL:** `https://workspace.vsco.co/api/v2`
- **Official documentation:** [Create Gallery](https://workspace.vsco.co/api/#operation/createResourceGallery)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | body | `string` | no | A ULID entity identifier that is nullable. |
| `eventId` | body | `string` | no | A ULID entity identifier that is nullable. |
| `remoteId` | body | `string` | no | The remote ID of this gallery. <b>This value must be unique for the studio.</b> |
| `remoteCreated` | body | `object` | no | — |
| `status` | body | `string` | no | — |
| `coverPhoto` | body | `object` | no | When creating or updating a gallery, this object may be used to import a cover photo. If the gallery does not yet have a covor photo, VSCO Workspace will use a placeholder graphic. |
| `public` | body | `boolean` | no | Whether this gallery is publicly accessible. |
| `requiresPassword` | body | `boolean` | no | — |
| `password` | body | `string` | no | A reusable plain-text passcode for unlocking the gallery. This pass code may be given to invited users. |
| `category` | body | `string` | no | The category of this gallery. Galleries may be grouped by this category text in future client portal designs. |
| `releaseDate` | body | `date` | no | The date this gallery will be released to the public. Useful in automations or email tokens. |
| `eventDate` | body | `date` | no | The date of the event this gallery is for. Useful in automations or email tokens. |
| `expirationDate` | body | `date` | no | The date this gallery will expire and no longer be accessible. Useful in automations or email tokens. |
| `orderDueDate` | body | `date` | no | The date that orders for this gallery are due by. Useful in automations or email tokens. |
| `orderCount` | body | `number` | no | The number of orders placed for this gallery. |
| `photoCount` | body | `number` | no | The number of photos in this gallery. |
| `visitorCount` | body | `number` | no | The number of visitors to this gallery. |
| `name` | body | `string` | yes | The name of this gallery. |
| `headline` | body | `string` | no | The headline of this gallery. Prioritized over name when displayed to the user. |
| `slug` | body | `string` | no | The URL path slug for this gallery. This is the URL-friendly version of the name and must contain only letters, numbers, dashes, and underscores. When setting this value, it will be converted to lowercase and any illegal characters stripped. |
| `clientUrl` | body | `string` | yes | The URL of this gallery. Will be used for links in emails and the client portal. |
| `adminUrl` | body | `string` | yes | The internal URL of this gallery in the remote admin portal. May be used to link employees to the gallery administration interface in the remote service. |
