# new-dhis-connector-dependencies
updated dhis connector dependencies

Follow the steps below to deploy the new version of dhis connector module.

Pull Serialized_Object or restore.

Run the following queries in openmrs db.

delete from liquibasechangelog where ID='20171128-2319'; \br
alter table dhisconnector_report_to_dataset modify location int(11) null; \br
alter table dhisconnector_report_to_dataset modify org_unit_uid text null; \br
