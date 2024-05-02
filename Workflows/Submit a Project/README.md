This is the primary workflow that partners use to submit a project. Here are some key features:
1. It allows for multiple shifts to be added to a project
2. It creates the project, shift(s), and associates the Team Lead properly as the leader for each occurrence
3. It uses ChatGPT to grammarize / spell check the Volunteer Resources and Project Description
4. Creates the connection request used for the approval process

### Actions to Review
#### Sign-Ups API Key
In order for the recently added team lead to be correctly associated to the newly created occurrence, you have to use the `groupmemberassignments` API since there is no workflow action that allows you to create this.

1. Create a REST key specifically for use with Sign-Ups
   - _This API key does not need to be added to any security roles for it to work_
2. Adjust its permissions so that it has access to the groupmemberassignments endpoint
   - Navigate to Security > REST Controllers
   - Find `GroupMemberAssignments` in the list and click into it
   - Edit security for the POST - api/GroupMemberAssignments
   - Add the profile associated with your REST key to View / Edit
3. You can either find / replace this: `signupAPIKey` in the JSON file with your API key or adjust the following actions if you've already imported it
   - Get First Shift Info > Associate Leader to the New Occurrence
   - Get Additional Shifts > Associate Leader to the New Occurrence

### Attributes to Review
#### Organization / Individual Name
We actually have two Defined Type lists that list Local Mission Partners and Local Organizations. If you don't have this, you can remove this from form action, otherwise you'll want to update the single select definition.

#### Sign-Up Parent Group
This was specified so we could create new projects precisely where we wanted them in the group tree to organize them. Adjust as needed.

#### Sign-Ups Team Leader Role
This should carry over, but verify that it is configured for the **Leader** role of the Sign-Up Group Type.

#### Project Characteristics
We maintain a list of characteristics in a Defined Type, adjust that here as needed.

#### AI Provider Key
If you want to use the ChatGPT support, add your AI API key as the default value to this attribute.

----------
There's also references to Serve Day, which just activates the "Serve Day" mode of the form. Feel free to utilize or ignore that piece.