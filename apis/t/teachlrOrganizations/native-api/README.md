# Teachlr Organizations: Native API Reference

A consolidated summary of Teachlr Organizations's API configuration and 38 documented operations, with links to official documentation.

- **Official docs:** https://soporte.teachlr.com/article-categories/documentacion-api/
- **API base URL:** `https://api.teachlr.com/mindcloudteachlr337933/api`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://soporte.teachlr.com/base-de-conocimientos/listar-los-cursos-de-una-escuela-usando-el-api-de-teachlr-organizaciones/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `last_page`. The current page number is read from `current_page`.

## Pagination

Use `limit` in the query string to set the page size (default 8; minimum 1). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Set the direction separately with `ord`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (38 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Meeting](actions/create-meeting.md) | `POST /meetings` | [docs](https://soporte.teachlr.com/base-de-conocimientos/creacion-actualizacion-y-eliminacion-de-videoconferencias-para-un-usuario-de-una-escuela-usando-el-api-de-teachlr-organizaciones-2/) |
| [Delete Meeting](actions/delete-meeting.md) | `DELETE /meetings/:meetingId` | [docs](https://soporte.teachlr.com/base-de-conocimientos/creacion-actualizacion-y-eliminacion-de-videoconferencias-para-un-usuario-de-una-escuela-usando-el-api-de-teachlr-organizaciones-2/) |
| [Filter And Export Transactions](actions/filter-and-export-transactions.md) | `GET /transactions` | [docs](https://soporte.teachlr.com/base-de-conocimientos/como-listar-las-transacciones-de-una-escuela-usando-el-api-de-teachlr-organizaciones-2/) |
| [Get Career Details Full](actions/get-career-details-full.md) | `GET /careers-online/:slug` | [docs](https://soporte.teachlr.com/base-de-conocimientos/como-obtener-los-detalles-de-una-carrera-de-una-escuela-usando-el-api-de-teachlr-organizaciones/) |
| [Get Course Details Full](actions/get-course-details-full.md) | `GET /courses-online/:slug` | [docs](https://soporte.teachlr.com/base-de-conocimientos/como-obtener-los-detalles-de-un-curso-de-una-escuela-usando-el-api-de-teachlr-organizaciones/) |
| [Get Course Details Localized](actions/get-course-details-localized.md) | `GET /courses-online/:slug` | [docs](https://soporte.teachlr.com/base-de-conocimientos/como-obtener-los-detalles-de-un-curso-de-una-escuela-usando-el-api-de-teachlr-organizaciones/) |
| [Get User by Email](actions/get-user-by-email.md) | `GET /users/query` | [docs](https://soporte.teachlr.com/base-de-conocimientos/como-obtener-la-informacion-de-un-usuario-de-una-escuela-usando-el-api-de-teachlr-organizaciones-usando-un-campo-identificador-del-usuario/) |
| [Get User By Employee Number](actions/get-user-by-employee-number.md) | `GET /users/query` | [docs](https://soporte.teachlr.com/base-de-conocimientos/como-obtener-la-informacion-de-un-usuario-de-una-escuela-usando-el-api-de-teachlr-organizaciones-usando-un-campo-identificador-del-usuario/) |
| [Get User By External Id](actions/get-user-by-external-id.md) | `GET /users/query` | [docs](https://soporte.teachlr.com/base-de-conocimientos/como-obtener-la-informacion-de-un-usuario-de-una-escuela-usando-el-api-de-teachlr-organizaciones-usando-un-campo-identificador-del-usuario/) |
| [Get User By Identifier With Certificates](actions/get-user-by-identifier-with-certificates.md) | `GET /users/query` | [docs](https://soporte.teachlr.com/base-de-conocimientos/como-obtener-la-informacion-de-un-usuario-de-una-escuela-usando-el-api-de-teachlr-organizaciones-usando-un-campo-identificador-del-usuario/) |
| [Get User By Username](actions/get-user-by-username.md) | `GET /users/:username` | [docs](https://soporte.teachlr.com/base-de-conocimientos/como-obtener-la-informacion-de-un-usuario-de-una-escuela-usando-el-api-de-teachlr-organizaciones/) |
| [Get User By Username With Certificates](actions/get-user-by-username-with-certificates.md) | `GET /users/:username` | [docs](https://soporte.teachlr.com/base-de-conocimientos/como-obtener-la-informacion-de-un-usuario-de-una-escuela-usando-el-api-de-teachlr-organizaciones/) |
| [Get User By Username Without Teaching](actions/get-user-by-username-without-teaching.md) | `GET /users/:username` | [docs](https://soporte.teachlr.com/base-de-conocimientos/como-obtener-la-informacion-de-un-usuario-de-una-escuela-usando-el-api-de-teachlr-organizaciones/) |
| [Invite Administrator](actions/invite-administrator.md) | `POST /invite` | [docs](https://soporte.teachlr.com/base-de-conocimientos/invitar-un-usuario-a-una-escuela-con-un-rol-usando-el-api-de-teachlr-organizaciones/) |
| [Invite Instructor](actions/invite-instructor.md) | `POST /invite` | [docs](https://soporte.teachlr.com/base-de-conocimientos/invitar-un-usuario-a-una-escuela-con-un-rol-usando-el-api-de-teachlr-organizaciones/) |
| [Invite User And Add To Groups](actions/invite-user-and-add-to-groups.md) | `POST /invitations` | [docs](https://soporte.teachlr.com/base-de-conocimientos/como-invitar-un-usuario-a-una-escuela-y-opcionalmente-suscribirlo-a-uno-o-varios-cursos-usando-el-api-de-teachlr-organizaciones/) |
| [Invite User And Subscribe To Careers](actions/invite-user-and-subscribe-to-careers.md) | `POST /invitations` | [docs](https://soporte.teachlr.com/base-de-conocimientos/como-invitar-un-usuario-a-una-escuela-y-opcionalmente-suscribirlo-a-uno-o-varios-cursos-usando-el-api-de-teachlr-organizaciones/) |
| [Invite User And Subscribe To Courses](actions/invite-user-and-subscribe-to-courses.md) | `POST /invitations` | [docs](https://soporte.teachlr.com/base-de-conocimientos/como-invitar-un-usuario-a-una-escuela-y-opcionalmente-suscribirlo-a-uno-o-varios-cursos-usando-el-api-de-teachlr-organizaciones/) |
| [Invite User And Sync Profile Fields](actions/invite-user-and-sync-profile-fields.md) | `POST /invitations` | [docs](https://soporte.teachlr.com/base-de-conocimientos/como-invitar-un-usuario-a-una-escuela-y-opcionalmente-suscribirlo-a-uno-o-varios-cursos-usando-el-api-de-teachlr-organizaciones/) |
| [Invite User With Role](actions/invite-user-with-role.md) | `POST /invite` | [docs](https://soporte.teachlr.com/base-de-conocimientos/invitar-un-usuario-a-una-escuela-con-un-rol-usando-el-api-de-teachlr-organizaciones/) |
| [List Active Courses](actions/list-active-courses.md) | `GET /courses/available` | [docs](https://soporte.teachlr.com/base-de-conocimientos/listar-los-cursos-de-una-escuela-usando-el-api-de-teachlr-organizaciones/) |
| [List All Non-Expired Courses](actions/list-all-non-expired-courses.md) | `GET /courses/all` | [docs](https://soporte.teachlr.com/base-de-conocimientos/listar-los-cursos-de-una-escuela-usando-el-api-de-teachlr-organizaciones/) |
| [List Careers](actions/list-careers.md) | `GET /careers` | [docs](https://soporte.teachlr.com/base-de-conocimientos/como-listar-las-carreras-de-una-escuela-usando-el-api-de-teachlr-organizaciones/) |
| [List Careers With Active Coupons](actions/list-careers-with-active-coupons.md) | `GET /careers` | [docs](https://soporte.teachlr.com/base-de-conocimientos/como-listar-las-carreras-de-una-escuela-usando-el-api-de-teachlr-organizaciones/) |
| [List Courses By Career](actions/list-courses-by-career.md) | `GET /courses/available` | [docs](https://soporte.teachlr.com/base-de-conocimientos/listar-los-cursos-de-una-escuela-usando-el-api-de-teachlr-organizaciones/) |
| [List Courses By Category And Subcategory](actions/list-courses-by-category-and-subcategory.md) | `GET /courses/available` | [docs](https://soporte.teachlr.com/base-de-conocimientos/listar-los-cursos-de-una-escuela-usando-el-api-de-teachlr-organizaciones/) |
| [List Courses By Instructor](actions/list-courses-by-instructor.md) | `GET /courses/available` | [docs](https://soporte.teachlr.com/base-de-conocimientos/listar-los-cursos-de-una-escuela-usando-el-api-de-teachlr-organizaciones/) |
| [List Courses With Active Coupons](actions/list-courses-with-active-coupons.md) | `GET /courses/available` | [docs](https://soporte.teachlr.com/base-de-conocimientos/listar-los-cursos-de-una-escuela-usando-el-api-de-teachlr-organizaciones/) |
| [List Deactivated Courses](actions/list-deactivated-courses.md) | `GET /courses/deactivated` | [docs](https://soporte.teachlr.com/base-de-conocimientos/listar-los-cursos-de-una-escuela-usando-el-api-de-teachlr-organizaciones/) |
| [List Draft Courses](actions/list-draft-courses.md) | `GET /courses/draft` | [docs](https://soporte.teachlr.com/base-de-conocimientos/listar-los-cursos-de-una-escuela-usando-el-api-de-teachlr-organizaciones/) |
| [List Paginated Careers Without Embedded Courses](actions/list-paginated-careers-without-embedded-courses.md) | `GET /careers` | [docs](https://soporte.teachlr.com/base-de-conocimientos/como-listar-las-carreras-de-una-escuela-usando-el-api-de-teachlr-organizaciones/) |
| [List Paginated Courses](actions/list-paginated-courses.md) | `GET /courses` | [docs](https://soporte.teachlr.com/base-de-conocimientos/listar-los-cursos-de-una-escuela-usando-el-api-de-teachlr-organizaciones/) |
| [List Pending Courses](actions/list-pending-courses.md) | `GET /courses/pending` | [docs](https://soporte.teachlr.com/base-de-conocimientos/listar-los-cursos-de-una-escuela-usando-el-api-de-teachlr-organizaciones/) |
| [List Public Library Careers](actions/list-public-library-careers.md) | `GET /careers/library` | [docs](https://soporte.teachlr.com/base-de-conocimientos/como-listar-las-carreras-de-una-escuela-usando-el-api-de-teachlr-organizaciones/) |
| [List Public Library Courses](actions/list-public-library-courses.md) | `GET /courses/library` | [docs](https://soporte.teachlr.com/base-de-conocimientos/listar-los-cursos-de-una-escuela-usando-el-api-de-teachlr-organizaciones/) |
| [List Transactions](actions/list-transactions.md) | `GET /transactions` | [docs](https://soporte.teachlr.com/base-de-conocimientos/como-listar-las-transacciones-de-una-escuela-usando-el-api-de-teachlr-organizaciones-2/) |
| [Search And Sort Courses](actions/search-and-sort-courses.md) | `GET /courses/available` | [docs](https://soporte.teachlr.com/base-de-conocimientos/listar-los-cursos-de-una-escuela-usando-el-api-de-teachlr-organizaciones/) |
| [Update Meeting](actions/update-meeting.md) | `PUT /meetings/:meetingId` | [docs](https://soporte.teachlr.com/base-de-conocimientos/creacion-actualizacion-y-eliminacion-de-videoconferencias-para-un-usuario-de-una-escuela-usando-el-api-de-teachlr-organizaciones-2/) |
