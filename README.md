# Developer-Console-Hacks

### Get the 18 digit Org ID for a Salesforce Org:
1.  Open the Developer Console
2.  From the Workspace Menu, choose 'Execute Anonymously'.
3.  Paste the following code:

    List<Organization> desiredInfoList = new List<Organization>();
    desiredInfoList = [SELECT Id from Organization];
    String desiredInfo = desiredInfoList[0].Id;
    system.debug(desiredInfo);
    
4. In the debug log, double click the result record and scroll until you get the OrgID in 18 digit format.

