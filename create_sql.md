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
