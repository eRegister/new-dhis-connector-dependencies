# new-dhis-connector-dependencies
updated dhis connector dependencies

Follow the steps below to deploy the new version of dhis connector module.


Pull Serialized_Object and restore.

Go to development_emr and glone this repository.
change directory to Omods and copy all omods files to /opt/openmrs/modules/

Run the following queries in openmrs db.

delete from liquibasechangelog where ID='20171128-2319'; 

alter table dhisconnector_report_to_dataset modify location int(11) null;

alter table dhisconnector_report_to_dataset modify org_unit_uid text null; 

restart openmrs.
