# Persisted Datasets
We use three different persisted datasets (in hindsight, maybe could've gotten away with two, but ¯\_(ツ)_/¯)

- Project Finder [Access Key: `projectfinder`]
   - _This one powers the public Sign-Up Finder block._
- Project Finder - Toolbox [Access Key: `projectfindertoolbox`]
   - _This one powers the Team Lead Toolbox, showing projects that are in the future but also those that happened within the last seven days._
- Email Preference Matching [Access Key: `projectfinderemailpreferences`]
   - _This one powers the logic behind the weekly tailored email to keep people informed about new projects that match their organization / characteristic preferences._

You'll find the lava for each of these in its own .lava file. Each one is configured like the image below, with descriptions / access keys differing.
![alt text](../Supporting%20Images/image.png)

# Example Elements in the Dataset
## Example element from `projectfinder`
```
{
    "GroupId": 307446,
    "ProjectKey": "2vnyBVO4Lo",
    "Guid": "62300432-3a36-4c1a-9b21-b824bf086956",
    "Name": "Harvest Blessing Day",
    "ProjectName": "Harvest Blessing Day",
    "ShiftName": "",
    "Image": "",
    "Description": "The Harvest Blessing Day project offers a no-commitment opportunity to volunteer and provide blessings to refugees and immigrants while gaining insight into the work of Refuge. Volunteers will gather at a designated church, where they will assemble small gifts for the individuals they will visit. These gifts will be accompanied by words of encouragement. Friends and family are welcome to join in these Blessing Day outings. The project aims to create a welcoming environment for immigrants and refugees in their new city, while also fostering friendships between volunteers and these families. It also provides an avenue for spiritual conversations and an opportunity to identify the needs of these families that Refuge could address through other available ministries. As a local ministry partner, we are dedicated to supporting and serving these communities. Participants are not required to bring anything, as all necessary materials will be provided.",
    "IsOnsite": false,
    "Schedule": "Saturday Oct 19 at 3:00 PM",
    "ScheduleKey": "V2RWVGa90M",
    "ScheduleAsDateTime": "2024-10-19T15:00:00-04:00",
    "Duration": "2 hrs",
    "Location": "Louisville, 40299",
    "LocationKey": "p79OxVxRvj",
    "FullAddress": "9105 Galene Dr
Encounter Church
Louisville, KY 40299-1523",
    "Organization": "Refuge International",
    "VolunteersBring": "Nothing",
    "ScheduleId": 7791,
    "LocationId": 58374,
    "ProjectType": "In-Person on the Project Date",
    "ProjectTypeId": "FF3F0C5C-9775-4A09-9CCF-94902DB99BF6",
    "MostNeeded": false,
    "PercentFilledDesired": 0.3,
    "PercentFilledMinimum": 1.5,
    "MinimumCapacity": 2,
    "DesiredCapacity": 10,
    "MaximumCapacity": 20,
    "PublishedDateTime": "2024-01-11T00:00:00",
    "ForServeDay": false,
    "ForGroupsThatServe": false,
    "CommunitySubmitted": true,
    "EmailPreferenceMatching": "3154,3148,2166",
    "AgeRequirement": "",
    "MemberQuantity": 3
  }
```
## Example element from `projectfindertoolbox`
```
{
    "GroupId": 309014,
    "ProjectKey": "lBRD4OOvR2",
    "Guid": "019f45a2-f54d-4d40-87f6-a486922d775a",
    "Name": "Meal Pack",
    "ProjectName": "Meal Pack",
    "ShiftName": "",
    "Image": "",
    "Description": "Volunteers will be participating in a project that involves packing over 80,000 meals during a span of three days in April. The main objective of this endeavor is to provide much-needed sustenance to individuals internationally, ultimately benefiting them by ensuring they receive proper nourishment. It is worth noting that participants are not required to bring anything along, as all the necessary materials and supplies will be provided.",
    "IsOnsite": true,
    "Schedule": "",
    "ScheduleKey": "pD94bKAnzX",
    "ScheduleAsDateTime": "",
    "Duration": "",
    "Location": "On Site at Northside",
    "LocationKey": "E2vnybLoK0",
    "FullAddress": "4407 Charlestown Rd
New Albany, IN 47150",
    "Organization": "Lifeline Christian Mission",
    "VolunteersBring": "Nothing",
    "ScheduleId": 8069,
    "LocationId": 2,
    "ProjectType": "In-Person on the Project Date",
    "ProjectTypeId": "FF3F0C5C-9775-4A09-9CCF-94902DB99BF6",
    "MostNeeded": false,
    "PercentFilledDesired": 0.61,
    "PercentFilledMinimum": 1.22,
    "MinimumCapacity": 40,
    "DesiredCapacity": 80,
    "MaximumCapacity": 80,
    "PublishedDateTime": "2024-02-05T00:00:00",
    "ForServeDay": true,
    "ForGroupsThatServe": false,
    "CommunitySubmitted": true,
    "EmailPreferenceMatching": "3130,3202,3158",
    "AgeRequirement": "",
    "OccurrenceConfirmationDetails": "
Please enter through Door #2 and head to the concrete Lobby.

",
    "OccurrenceReminderDetails": "
Please enter through Door #2 and head to the concrete Lobby.

",
    "MemberQuantity": 49
  }
```
## Example element from `projectfinderemailpreferences`
```
{
    "Guid": "62300432-3a36-4c1a-9b21-b824bf086956",
    "PreferenceId": "3154"
  }
```