# Project_1_Group_22

the database, including tables, attributes, primary keys, foreign keys, foreign key constraints, functional dependencies (FDs), and sample data for each table.

Database Description:
Tables:
Bikes:

Attributes: BikeID (Primary Key), BikeName, RentalPricePerHour, AvailabilityStatus
Primary Key: BikeID
Foreign Keys: None
Foreign Key Constraints: None
FDs: {BikeID} -> {BikeName, RentalPricePerHour, AvailabilityStatus}
Sample Data:
BikeID	BikeName	RentalPricePerHour	AvailabilityStatus
1	Mountain Bike	10.00	TRUE
2	City Bike	8.00	TRUE
Rentals:

Attributes: RentalID (Primary Key), BikeID (Foreign Key), CustomerName, RentalDurationInHours
Primary Key: RentalID
Foreign Keys: BikeID references Bikes(BikeID)
Foreign Key Constraints: When a rental is added or removed, AvailabilityStatus in Bikes table is updated.
FDs: {RentalID} -> {BikeID, CustomerName, RentalDurationInHours}
Sample Data:
RentalID	BikeID	CustomerName	RentalDurationInHours
1	1	Alice	3
2	3	Bob	2
Employees:

Attributes: EmployeeID (Primary Key), EmployeeName, EmployeeRole, Salary
Primary Key: EmployeeID
Foreign Keys: None
Foreign Key Constraints: None
FDs: {EmployeeID} -> {EmployeeName, EmployeeRole, Salary}
Sample Data:
EmployeeID	EmployeeName	EmployeeRole	Salary
1	John	Manager	50000.00
2	Lisa	Sales Associate	35000.00
Services:

Attributes: ServiceID (Primary Key), EmployeeID (Foreign Key), ServiceType, ServiceCharge
Primary Key: ServiceID
Foreign Keys: EmployeeID references Employees(EmployeeID)
Foreign Key Constraints: None
FDs: {ServiceID} -> {EmployeeID, ServiceType, ServiceCharge}
Sample Data:
ServiceID	EmployeeID	ServiceType	ServiceCharge
1	3	Repair	50.00
2	2	Consultation	30.00
This description outlines the structure of the database, including tables, attributes, primary keys, foreign keys, foreign key constraints, and functional dependencies. It also includes a few rows of sample data for each table to illustrate how the tables are populated.



CREATE TABLE Bikes (
    BikeID INT PRIMARY KEY,
    BikeName VARCHAR(255),
    RentalPricePerHour DECIMAL(10, 2),
    AvailabilityStatus BOOLEAN
);

CREATE TABLE Rentals (
    RentalID INT PRIMARY KEY,
    BikeID INT,
    CustomerName VARCHAR(255),
    RentalDurationInHours INT,
    FOREIGN KEY (BikeID) REFERENCES Bikes(BikeID)
);

CREATE TABLE Employees (
    EmployeeID INT PRIMARY KEY,
    EmployeeName VARCHAR(255),
    EmployeeRole VARCHAR(255),
    Salary DECIMAL(10, 2)
);

CREATE TABLE Services (
    ServiceID INT PRIMARY KEY,
    EmployeeID INT,
    ServiceType VARCHAR(255),
    ServiceCharge DECIMAL(10, 2),
    FOREIGN KEY (EmployeeID) REFERENCES Employees(EmployeeID)
);
