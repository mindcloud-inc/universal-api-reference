# Rentman Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Rentman expects, and each action page lists the fields available to sort.

## Rentman actions that support sorting

- [List Appointments](actions/list-appointments.md)
- [List Contact Persons](actions/list-contact-persons.md)
- [List Contacts](actions/list-contacts.md)
- [List Crew](actions/list-crew.md)
- [List Crew Rates](actions/list-crew-rates.md)
- [List Equipment](actions/list-equipment.md)
- [List Equipment Serial Numbers](actions/list-equipment-serial-numbers.md)
- [List Invoices](actions/list-invoices.md)
- [List Project Crew](actions/list-project-crew.md)
- [List Project Equipment](actions/list-project-equipment.md)
- [List Project Functions](actions/list-project-functions.md)
- [List Project Subprojects](actions/list-project-subprojects.md)
- [List Projects](actions/list-projects.md)
- [List Vehicles](actions/list-vehicles.md)
