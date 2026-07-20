# Publish Post with AnnounceKit

Creates and publishes a post in AnnounceKit.

## Endpoint

- **Method:** `POST`
- **Path:** `/gq/v2`
- **Base URL:** `https://announcekit.app`
- **Official documentation:** [Publish Post](https://announcekit.app/docs/graphql-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | yes | AnnounceKit project id that will receive the published post. Defaults to the project id provided for this build. |
| `title` | body | `string` | yes | Title for the AnnounceKit post content. |
| `body` | body | `string` | yes | HTML body for the AnnounceKit post content. AnnounceKit documents support for basic HTML tags. |
| `locale_id` | body | `string` | yes | Locale id for the post content. The AnnounceKit example uses en. |
