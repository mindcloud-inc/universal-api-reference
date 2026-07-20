# Add Multiple Subscribers with Moosend

Creates multiple subscribers in Moosend.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers/{{MailingListID}}/subscribe-many.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [Add Multiple Subscribers](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54576-Add-multiple-subscribers?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `MailingListID` | path | `string` | yes | The ID of the email list where you want to add multiple subscribers. |
| `HasExternalDoubleOptIn` | body | `boolean` | no | When true , it flags the added subscribers as having given their subscription consent by other means. |
| `Subscribers` | body | `list<object>` | yes | A list containing up to 1000 subscribers that you are adding to the email list. You must specify the Name , Email , and CustomFields for each subscriber. |
| `Tags` | body | `object` | no | The member tag you can use to filter members by when working with an email list. |
| `Preferences` | body | `object` | no | The member preferences you can user to segment or filter members by, when working with an email list. |
