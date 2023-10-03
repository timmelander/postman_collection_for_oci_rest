# POSTMAN COLLECTION FOR INVOKING Oracle OCI REST APIs
Associated blog post : https://link.medium.com/sCcFWZU68W and http://www.ateam-oracle.com/invoking-oci-rest-apis-using-postman 

**UPDATES:** 
* Fixed OCI Collection Pre-request Script per https://developer.oracle.com/learn/technical-articles/making-calls-to-oci-api-with-postman
* Updated variable names in Collection Pre-request Script and Environment to make more sense in relation to the data required.
* Added sample IAM Identity Domain requests with reusable variables. 

**OVERVIEW:**
* Updates in Javascript on improvements co-authored by Manansi Vaishampayan and Tim Melander.
* Youtube : https://www.youtube.com/watch?v=8x1-3-k0poM

**INSTRUCTIONS:**

1. Download the repository's Postman collections and environment.

2. Import the environment into Postman using the ‘Import’ button at the top, and activate it by selecting it from the top right drop-down. 

3. Open and Edit the newly imported environment, and set the OCI REST variables USER_OCID, TENANCY_OCID, REGION, COMPARTMENT_OCID, PRIVATE_KEY, FINGERPRINT, optionally PASSPHRASE. Additionally update the IDCS_HOST variable if using the IAM Identity Domain collection requests examples.

4. Now import the OCI_REST_COLLECTION collection into Postman.

5. From the collection invoke the ONE_TIME_INITIALIZATION_CALL Initializer GET for ‘jsrsasign-all-min.js’ , which imports and initializes a required library jsrsasign for encryption and digital signatures. This is a one-time setup task.

6. Test by running the GET_OCI_ANNOUNCEMENTS request.

That’s it!! Now you can use the other oci_rest_collection to invoke any OCI REST APIs. The collection provides a sample GET and POST request, which can be extrapolated to invoke any OCI REST API.

Just make sure that the OCI REST calls are executed as part of the OCI_REST_COLLECTION, as that collection contains the necessary javascript code to generate OCI’s authentication header
