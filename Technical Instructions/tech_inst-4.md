### Test #6001

Verify that PDQ Consumer can submit a Patient Demographics Query (ITI-47) transaction
In these test, you will use the Patient Manager as a Patient Demographics Supplier (PDS) Simulator to respond to your PDQ Query.

**References:** ITI TF-2b 3.47 and ITI TF-2x O.1.1

**Actor:** Patient Demographics Consumer

**Dependencies:** None

**Resources:** [Gazelle Patient Manager](https://gazelle.ihe.net/PatientManager/hl7v3/pdq/supplier.seam)

**Test Procedure**

1. Access the Patient Manager tool: [http://gazelle.ihe.net/PatientManager](http://gazelle.ihe.net/PatientManager)
 
2. Go to menu All Patients. Next, in the drop-down box "Simulated actor", select PDS - Patient Demographic Supplier.  The page then lists the patients known by the PDQ Supplier simulator.
Choose one or more of the available patients to use as the target for your query in  this test.

![](./media/image4-1.png)

3. Go to menu PDQ-->Patient Demographic Supplier (PDS). Next, select HL7v3 Configuration.  

4. The tool will display the configuration details you will need to query the PDS Simulator. Ensure the status of the Simulator is "Running".

![](./media/image4-2.png)

5. Configure your System Under Test (SUT) to perform query based on the PDS simulator endpoint (collected on Item d). Pay attention to the ITI TF-2b Table 3.47.4.1.2.3-1: Wrappers and Constraints. See example on this [SOAPUI project](./SOAPUI%20Projects/Gazelle-Patient-Manager-examples-soapui-project).

6. You can use menu HL7 messages to find the query & response captured by the tool

![](./media/image4-3.png)

7. Take a screenshot of your application or your database as a proof of receipt of the query response. Retrieve the permanent link to the transaction instance, and paste that as evidence for this test. The screen shot demonstrates that you have successfully processed the received query response(s).

Note 1:  This simulator it will not work if you send an ITI-44 Patient Add and try to retrieve the same patient. Only patients known by the PDQ Supplier simulator can be retrieved. 

Note 2: You can use the menu “Messages Browser” to inspect and validate your messages. Click on the magnifying glass icon to inspect messages.

![](./media/image4-4.png)

When inspecting messages you will have the option to verify the validation results.

![](./media/image4-5.png)

### Test #6002

Verify that PDQ Consumer can submit a Patient Demographics Query HL7V3 Continuation transaction. In these test, you will use the Patient Manager as a Patient Demographics Supplier (PDS) Simulator to respond to your PDQ Query.

**References:** ITI TF-2b 3.47.4.3 and ITI TF-2x O.1.3

**Actor:** Patient Demographics Consumer

**Dependencies:** None

**Resources:** [Gazelle Patient Manager](https://gazelle.ihe.net/PatientManager/hl7v3/pdq/supplier.seam)

**Test procedure**   

1. Access the Patient Manager tool: [http://gazelle.ihe.net/PatientManager](http://gazelle.ihe.net/PatientManager).  

2. Go to menu PDQ-->Patient Demographic Supplier (PDS). Next, select HL7v3 Configuration.

3. The tool will display the configuration details you will need to query the PDS Simulator. Ensure the status of the Simulator is "Running".

![](./media/image4-6.png)

4. Configure your System Under Test (SUT) to perform query based on the PDS simulator endpoint (collected on Item c). Pay attention to the ITI TF-2b Table 3.47.4.3.2.3-1: Wrappers and Constraints.

5. Your message should include a LivingSubjectName with given equal to “Jo” as part of the ParameterList class. Also, configure your message to retrieve 10 patients at maximum (“InitialQuantity” with value=10).  See examples on this [SOAPUI project](./SOAPUI%20Projects/Gazelle-Patient-Manager-examples-soapui-project).

6. You can use menu HL7 messages to find the query & response captured by the tool. Similar to what was done in the previous test (Test #6001).

7. Take a screenshot of your application or your database as a proof of receipt of the query response. Retrieve the permanent link to the transaction instance, and paste that as evidence for this test. The screen shot demonstrates that you have successfully processed the received query response(s).