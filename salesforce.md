```JS
Roll-Up Summary fields are available on the master object when there is a Master-Detail relationship. Since Loan is the master and Payment is the detail, we can calculate values such as total payment amount on the Loan record.
```

```JS
Q1. What is a Roll-Up Summary field?
Answer: A Roll-Up Summary field calculates aggregated
values from related detail records and displays the result on the master record.”


Lookup
❌ Roll-Up Summary normally not available

Master-Detail
✅ Roll-Up Summary available

What is the difference between a Lookup Relationship and a Master-Detail Relationship in Salesforce?

e use lookup because a customer can have multiple loans, and the loan record is related but not dependent on the customer.” Aur haan—yahi one-to-many case lookup ya master-detail dono se model ho sakta hai, but humne yahan independence chahiye thi, isliye lookup choose kiya.
We use a Master-Detail relationship between Loan and Payment because a Payment is dependent on a Loan and cannot exist independently. Loan is the master, and Payment is the detail. If the Loan is deleted, its related Payments are also deleted.”

What is a Roll-Up Summary field in Salesforce, and why did we use it in our Loan object
A Roll-Up Summary field is available on the master object in a Master-Detail relationship. It is used to calculate aggregate values from related detail records, such as SUM, COUNT, MIN, or MAX. In our project, we used it on the Loan object to calculate the total payment amount from its related Payment records.

Can a Roll-Up Summary field be created on a Lookup Relationship? Why or why not?
No, a Roll-Up Summary field cannot normally be created on a Lookup Relationship because Roll-Up Summary requires a Master-Detail relationship. In our project, we use Master-Detail between Loan and Payment, so we can calculate the total payment amount on the Loan.

An Object is similar to a table in a database. A Record is an individual row or entry in that object, and a Field is a column that stores a specific piece of information about the record.”

A Salesforce Org is a complete Salesforce environment provided to an organization. It contains its users, data, objects, fields, configurations, automation, and security settings.”


What is the difference between a Profile and a Permission Set in Salesforce?

A Profile is the baseline permission set for a user. It defines the user's default access, such as object permissions, field-level security, and system permissions. A Permission Set is used to grant additional permissions to a user without changing their profile.”

A Profile controls what a user can do in Salesforce, such as which objects, fields, and records they can access or modify. A Role mainly controls which records a user can see through the role hierarchy. In simple terms, Profile defines the user’s permissions, while Role helps determine record visibility.”

Governor Limits are runtime limits imposed by Salesforce to ensure that one transaction does not consume excessive shared resources. They limit things like the number of SOQL queries, DML statements, and CPU time that can be used in a transaction.”

Why does Salesforce have them?

Salesforce is a multi-tenant platform, meaning many customers share the same infrastructure.

So Salesforce uses Governor Limits to make sure:

One organization's code cannot consume all the resources and negatively affect other organizations.

```
### sObject
```
sObject ⭐⭐⭐

Now we reach one of the most important Apex concepts. sObject represents a Salesforce record.
For example, our custom object: Loan__c loan = new Loan__c();

```

### DML

```
Now let's understand DML properly
insert is one of the DML operations in Apex.
The main ones you need to know are: insert, update, delete, undelete, upsert
insert Command : insert loan
update command : loan.Loan_Status__c = 'Closed' -> update loan;
delete Commmand : delete loan
undelete loan : Restores a deleted record if it's recoverable from the Recycle Bin.
upsert loan : Creates the record if it doesn't exist, or updates it when the matching external ID condition is met.
```
