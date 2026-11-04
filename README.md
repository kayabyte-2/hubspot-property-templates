# HubSpot property CSV templates

Small, ready-to-edit CSV files for creating HubSpot properties, property groups and dropdown options in one go instead of one at a time in the property editor.

The files use the column layout of Bulk Property Import & Export, an app for HubSpot that I (Kayabyte) built. Full disclosure: it is our app. The CSVs are plain text, so you can also use them as a checklist and create the properties by hand.

## Files

- `templates/deal-qualification.csv`: budget, decision maker, buying timeline and a lost-reason text field on deals.
- `templates/contact-lead-source.csv`: lead source detail, campaign and preferred language on contacts.
- `templates/company-account-fields.csv`: account tier, renewal date and customer health on companies.

## Columns

`object` (contacts, companies, deals), `name` (internal name, lowercase with underscores), `label`, `type`, `field_type`, `group`, `group_label`, `description`, `options`, `options_mode`, `action`.

In `options`, put one option per line as `Label|internal value`. `options_mode` is `merge` (add and relabel, keep the rest) or `replace`. `action` is `upsert`, `create`, `update` or `skip`.

## Using them

1. Edit the file: rename groups and options to what your team uses.
2. Install Bulk Property Import & Export from the HubSpot Marketplace: https://ecosystem.hubspot.com/marketplace/listing/bulk-property-import-export
3. Paste or upload the CSV. The app first shows a preview of what will be created or changed; nothing is written until you click Apply.

The app is free for import, export and preview. More: https://kayabyte.dev/hubspot/bulk-property/

Without the app: HubSpot's property editor takes one property at a time, and its import tool can create properties from columns in a contact, company or deal import file.

## Notes

These are examples, not a recommended data model. Check the internal names do not clash with properties you already have. HubSpot is a registered trademark of HubSpot, Inc.; this repository is not affiliated with or endorsed by HubSpot.

License: MIT.
