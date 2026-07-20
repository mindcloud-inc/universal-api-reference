# Create Form with Google Forms

Creates a new empty form in Google Forms.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://forms.googleapis.com/v1/forms`
- **Official documentation:** [Create Form](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `info.title` | body | `string` | yes | Visible title for responders. Google Forms create copies this field. |
| `info.documentTitle` | body | `string` | no | Optional Drive document title for the new form. Google allows this only during form creation. |
| `unpublished` | query | `boolean` | no | When true, creates the form unpublished so it does not accept responses yet. |
