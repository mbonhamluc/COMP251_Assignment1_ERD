# Assignment 1 - Creating an ER Diagram for MPLSRenters.com
This assignment will meet each of the objectives below:
1. Translate business use cases for data into entity relationships

2. Determine appropriate entity structure for relational databases

3. Apply the correct terminology to a ER Model

4. Design an ER model

## Instructions
For this assignment, your task is to analyze the provided business description and identify the necessary business rules to create an ER diagram. These rules will encompass relationships, constraints, and data requirements.

You are required to compile a README.md file, which will detail each entity along with a brief description of its purpose and the data it collects. Additionally, identify the relationships between entities and note any assumptions or questions you may have for the client based on the business description. You will also decide the answers to your assumptions on behalf of the client.

After completing the README.md file, your next step is to construct an ER Diagram based on the identified relationships from the business description. This diagram should be created using a free web-based tool called 'draw.io.' You'll find the shapes needed for your ER diagram under the 'Entity Relation' tab. Instructions on how to operate draw.io can be found in the assignment resources section below. **DRAW.IO must be used as your ER diagram tool**

## Business Description
MPLSRenters.com is a website that allows prospective apartment renters to create a profile and have
high-end luxury apartments make offers to prospective renters.

1.  A property can have many high-end amenities associated with it. The amenities that are
associated with a property are preset amenities that can be added to a property.  Each amenity will have a name and description. 
 If properties have unique amenities that are not a part of the preset amenities, then those details will go into
the long description for each property. A property will contain information such as first and last name, email, phone, address, short and long description, longitude/latitude of property, and rent range (the lowest and highest amount you can expect to pay).
2. Prospective renters can add as many amenities to their profile as they deem necessary. The amenities will
be the same preset amenities that can be added to a property.  A renter will collect the same information a property would collect, but will also include a renter's decision date, the number of bedrooms and bathrooms, and the lower and max rent value they are willing to spend.  
3. Prospective renters can add as many properties to their profile as they desire. A prospective renter can exist in the system without having a property associated with a profile.
4. A property can have multiple property agents associated with a property. A property does not
have to be associated with a property agent to exist within the database. Property agents can
be activated and deactivated from the system based on whether or not payment for a monthly
package was made on time.
5. Both a profile and a property can receive a classification. There are only three pre-determined
classifications that can be associated with a profile or property. A profile is classified based on
the lower and upper range a prospective renter is looking to have for monthly rent. A
property is classified based on the select amenities, square footage, and lower/upper rent range. Each classification will contain a title, description, and a classification identifier (ex.  A high-luxury, B high - mid-luxury, or C luxury property)
6. A property agent can sign-up for one of three packages. All property agents must have an agent
package. An agent package determines how much access they will be granted to user profile
information.  An Agent package will contain a name, the package description, and an agent option selection (monthly payment package or yearly payment package)
7. Property agents are able to make multiple offers to those who have profiles in the system. A
profile can receive multiple offers from an agent. A profile can decline or entertain an offer.  An offer will contain information such as a description of the offer, the offer expiration date, and the property name for which the offer is being made.

## Submission Guidelines

For this assignment, you will submit 2 items to the repository that has been assigned to you.  The two items that you will need to submit are listed below: 
1. The README.MD file that identifies the various Entities and a brief description of the entity and possible attributes, relationships, and assumptions. 
   1. When identifying relationships be sure to bold and uppercase the entity name, underline the verb and make sure relationships are bi-directional. 
   2. When identifying assumptions, make sure to answer your assumption with either a Yes or No and make sure your response is properly reflected in the ER diagram.  
   3. You can override this README.MD file that contains the instructions or extend this README.MD file by listing your requirements below the Assignment Resources section.

2. The draw.io XML file that contains your ER Diagram.  You will also need to take a snippet of the ER Diagram and add it as an image in your README file.

Once you have completed both of the items above, you will need to submit the link to your repository for assignment 1 prior to the due date and time listed.  Make sure you receive an email confirmation notifying you that the assignment has been submitted.

### Rubric
| Criteria           | Description                             | Points |
| -------------------| --------------------------------------- | ------ |
|**Deliverable 1 - Write-up documented in README.md file**   | Write-up identifies the various entities with brief description (4pts) <br> Write-up identifies the various relationships that exist between the entities (6pt) <br> Write-up list assumptions that provides context for cardinality and entity strength (2 pts) <br> Write-up contains uppercase entity names, underlined verb and relationships are bi-directional (3 pts)  |   15   |
|**Deliverable 2 - Properly structured ER diagram** | All Entities identified in deliverable 1 are visually represented in Workbench ER diagram. (4pts) <br> Relationship strength is indicated by solid or dotted line (2pt) <br> Foreign keys and Primary keys are identified and correctly assigned (2 pts) <br> Each column name indicates null vs not null (2pt) <br> Image of ER diagram is depicted in README.MD file (2 pt) <br> Associative entities are identified and properly captures the relationship between the two entities(3 pts)   |   15   |
|           |        |**Total Points:   30**   |


## Assignment Resources
- [Mark-down Syntax Cheat Sheet](https://enterprise.github.com/downloads/en/markdown-cheatsheet.pdf)
- [Make a ReadMe file Web-based Editor](https://www.makeareadme.com/)
- [Draw.io Web-based diagramming tool](https://app.diagrams.net/)
- [Creating Entity Relationship Diagrams using Draw.io](https://www.youtube.com/watch?v=lAtCySGDD48)

## Completed Work

### Requirements

#### Entity Descriptions

- **CONTACT** is basic contact information for a person who may be a representative for a **PROPERTY**, A prospective renter in a **RENTER**, or a **AGENT**. The **CONTACT** has:
  - A `ContactID` that provides a unique identifier for the **CONTACT**.
  - A `FirstName` that is the first part of the name of the **CONTACT**.
  - A `LastName` that is the second part of the name of the **CONTACT**.
  - An `email` address that allows someone to connect with the **CONTACT**.
  - A `phone` number that is the number someone can use to connect with the **CONTACT**.
  - An `AddressLine1` which is the first line of the **CONTACT** address. Usually contains a street number and street.
  - An `AddressLine2` which is the second line of the **CONTACT** address. Usually contains an apartment number and is optional.
  - An `AddressCity` that is the city of the **CONTACT** address.
  - An `AddressState` which is the state of the **CONTACT** address. 
  - An `AddressZip` that is the zip code of the **CONTACT** address. 
- **PROPERTY** is a luxury apartment offered on the MPLSRenters.com website. The **PROPERTY** has:
  - A `PropertyID` that provides a unique identifier for each **PROPERTY**
  - A `ContactID` that is the unique id in the **CONTACT** table for the representative for the **PROPERTY**.
  - A `ClassificationID` that is the unique id in the **CLASSIFICATION** table for the **PROPERTY**
  - A `PropertyName` that is the name of the **PROPERTY**.
  - A `ShortDescription` that briefly describes the **PROPERTY**.
  - A `LongDescription` that describes the property in glonger form. This field may also contain amenties offered by the **PROPERTY** that are not in the pre-defined **AMENITY** list.
  - A `Longitude` which is one of two decimal numbers that simplifies finding the **PROPERTY** through a digital map via the use of digital coridinates.
  - A `Latitude` which is one of two decimal numbers that simplifies finding the **PROPERTY** through a digital map via the use of digital coridinates.
  - A `MinimumRent` which is a decimal number with two digits of precision that is the lowest rent amount for the **PROPERTY**.
  - A `MaximumRent` which is a decimal number with two digits of precision that is the highest rent amount for the **PROPERTY**.
  - `SqFoot` is a whole number that is the square footage of the property and used in calculating **CLASSIFICATION** as assigned.
- **AMENITY** is a pre-defined list of features or services offered by a **PROPERTY** or that may be of interest to a **RENTER**. The **AMENITY** has:
  - An `AmenityID` that provides a unique identifier for each **AMENITY**
  - A `Name` that identifies it.
  - A `Description` that explains what the **AMENITY** is.
- **PROPERTYAMENITY** connects **PROPERTY**s to associated **AMENITY**s that they offer. It contains fields that associate including:
  - A `PropertyID` which identifies the specific **PROPERTY** in this association.
  - An `AmenityID` which identifies the specific **AMENITY** in this association or the amenity the property offers.
- **RENTER** is a prospective renter that has signed up to use the website and is looking to find a **PROPERTY** and expresses interest in **AMENITY**s. The **RENTER** has:
  - A `RenterID` that provides a unique identifier for each **RENTER**
  - A `ContactID` that is the unique id in the **CONTACT** table for the **RENTER**
  - A `ClassificationID` that is the unique id in the **CLASSIFICATION** table for the **RENTER**
  - A `DecisionDate` which is the date the **RENTER** plans to make a decision by.
  - A `BedroomNumber` which is the number of bedrooms the **RENTER** needs.
  - A `BathroomNumber` which is the number of bathrooms the **RENTER** needs.
  - A `MinimumRent` which is a decimal number with two digits of precision that is the lowest rent amount the prospective **RENTER** is willing to spend.
  - A `MaximumRent` which is a decimal number with two digits of precision that is the highest rent amount the prospective **RENTER** is willing to spend.
- **RENTERAMENITY** connects **RENTER**s to associated **AMENITY**s they are interested in. It contains fields that associate including:
  - A `RenterID` which identifies the specific prospective **RENTER** in this association.
  - An `AmenityID` which identifies the specific **AMENITY** in this association or the amenity the prosepective renter has interest in.
- **RENTERPROPERTY** connects **RENTER**s to associated **PROPERTY**s they are interested in. It contains fields that associate including:
  - A `RenterID` which identifies the specific prospective **RENTER** in this association.
  - An `PropertyID` which identifies the specific **PROPERTY** in this association or the property the prosepective renter has interest in.
- **AGENT** is an agent who represents one or more **PROPERTY**s and can make rental **OFFER**s on their behalf. The **AGENT** has:
  - A `AgentID` that provides a unique identifier for each **AGENT**
  - `ContactID` that is the unique id in the **CONTACT** table for the **AGENT**
  - `IsActive` identifies if the **AGENT** can use the system based on system logic that identifies if payment was recieved on time.
  - `AgentPackageID` thatis a required foreign key that identifies the **AGENTPACKAGE** selected by the agent.
- **AGENTPROPERTY** connects **PROPERTY** to associated **AGENT** they sell for.It contains fields that associate including:
  - `AgentID` identifies the **AGENT** assigned to the property.
  - `PropertyID` identifies the **PROPERTY** the agent sells for.
- **CLASSIFICATION** is a lookup table that defines the three preset luxury categories a **RENTER** profile or a **PROPERTY** can receive. A renter profile’s classification is based on the renter’s desired monthly rent range. A property’s classification is based on its selected amenities, square footage, and monthly rent range.
  - `ClassificationID` uniquely identifies the category using a value of A, B, or C.
  - `Title` names the class using the values “High Luxury,” “High-Mid Luxury,” or “Luxury” respectively.
  - `Description` explains what the category means.
- **AGENTPACKAGE** defines one of the three preset packages a **AGENT** can select. The package determines how much information the agent can view in a **RENTER** profile. Each **AGENTPACKAGE** has the following attributes:
  - `AgentPackageID` that provides a unique identifier for each **AGENTPACKAGE**
  - A `Name` gives the name of the package.
  - `Description` explains what the package includes.
  - `IsMonthly` says whether the package is billed monthly or yearly. If true then this is a monthly plan. Otherwise it is yearly.
- **OFFER** records an individual offer a **AGENT** makes to a **RENTER** for a specific **PROPERTY**. The same agent may make multiple offers to the same renter. Each **OFFER** has the following attributes:
  - An `OfferID` that provides a unique identifier for each **OFFER**
  - `AgentID` is a required foreign key that identifies the **AGENT** who made the offer.
  - `RenterID` is a required foreign key that identifies the **RENTER** who received the offer.
  - `PropertyID` is a required foreign key that identifies the **PROPERTY** for which the offer was made.
  - `Description` describes what the **AGENT** is offering to the **RENTER**.
  - `ExpirationDate` gives the date the offer expires.
  - `IsDeclined` records whether the **RENTER** declined or entertained the offer. It is NULL until the **RENTER** responds. When the **RENTER** does responed it will be false if they entertained and true if they declined.

#### Relationships

- A **CONTACT** may <ins>represent</ins> zero or more **PROPERTIES**.	Each **PROPERTY** must be <ins>represented</ins> by exactly one **CONTACT**.
- A **CONTACT** may <ins>belong</ins> to zero or one **RENTER** profile.	Each **RENTER** profile must <ins>belong</ins> to exactly one **CONTACT**.
- A **CONTACT** may <ins>belong</ins> to zero or one **AGENT** record.	Each **AGENT** record must <ins>belong</ins> to exactly one **CONTACT**.
- A **PROPERTY** may <ins>offer</ins> zero to many **AMENITY**s; An **AMENITY** may be <ins>offered</ins> at zero to many **PROPERTY**s.
- A **RENTER** may be <ins>interested</ins> in zero to many **AMENITY**s; An **AMENITY** may be of <ins>interest</ins> to zero to many **RENTER**s.
- A **RENTER** may be <ins>interested</ins> in zero to many **PROPERTY**s; A **PROPERTY** many be of <ins>interest</ins> to zero to many **RENTERS**.
- A **PROPERTY** may be <ins>represented</ins> by zero or more **AGENT**s. Each **AGENT** must <ins>represent</ins> one or more **PROPERTIES**.
- A **CLASSIFICATION** may <ins>apply</ins> to zero or more **RENTER** profiles. Each **RENTER** profile may <ins>apply</ins> to zero or one **CLASSIFICATION**.
- A **CLASSIFICATION** may <ins>apply</ins> to zero or more **PROPERTIES**. Each **PROPERTY** may <ins>apply</ins> to zero or one **CLASSIFICATION**.
- A **AGENT** must <ins>select</ins> exactly one **AGENTPACKAGE**. An **AGENTPACKAGE** may be <ins>selected</ins> by zero or more AGENTS.
- A **AGENT** may <ins>make</ins> zero or more **OFFER**a. Each **OFFER** must be <ins>made</ins> by exactly one **AGENT**.
- A **RENTER** may <ins>receive</ins> zero or more **OFFER**s. Each **OFFER** must be <ins>received by</ins> exactly one **RENTER**.
- A **PROPERTY** may <ins>have</ins> zero or more **OFFER**s. Each **OFFER** must <ins>have</ins> exactly one **PROPERTY**.

#### Assumptions

- Is the `FirstNName` and `LastName` associated with a **PROPERTY** the name of the representative of that property and not the name of the **PROPERTY** itself? **YES**
- Are `MinimumRent` and `MaximumRent` always in US dollars? **YES**
- Are **PROPERTY** addresses always within the US? **YES**
- Can a **PROPERTY** have zero **AMENITY**s? **YES**
- Can a prospective **RENTER** have no **AMENITY**s associated with them? **YES**
- Though a renter may have the same information as a **PROPERTY**, this doesn't apply to the attibutes `ShortDescription`, `LongDescription`, `Longitude`, or `Latitude`, correct? **YES**
- Can an **AGENT** represent more than one **PROPERTY**? **YES**
- A **AGENT** should have **CONTACT** information like name, address, email, and the like, correct? **YES**
- Though `IsActive` is determined programatically in the system, it is fine to persist the systemic result in a table for ease of processing and simpler reporting? **YES**
- For **CLASSIFICATION**, the use of the one letter A, B, or C is sufficent as an identifier? **YES**
- You stated that a **RENTER** or **PROPERTY** can recieve a **CLASSIFICATION**. Can I assum that the use of the word <ins>can</ins> means that it might not? **YES**
- Though the assignment of a **CLASSIFICATION** to a **RENTER** or **PROPERTY** is determined programatically in the system using the logic you specified, it is fine to persist the systemic result in a table for ease of processing and simpler reporting? **YES**
- For the **AGENTPACKAGE**, the assignment of that package is sufficent to set authorization in the system. In other words, the system looks at the assigned package programatically and provides the **AGENT** access. No additional tables are needed to define fine grained authorization, correct? **YES**
- May an **AGENT** make an **OFFER** only for a **PROPERTY** they represent? **YES**

### Entity Relationship Diagram(ERD)