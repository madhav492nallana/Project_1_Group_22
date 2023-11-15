-- Insert data into Bikes table
INSERT INTO Bikes (BikeID, BikeName, RentalPricePerHour, AvailabilityStatus) VALUES
(1, 'Mountain Bike', 10.00, TRUE),
(2, 'City Bike', 8.00, TRUE),
(3, 'Road Bike', 12.00, FALSE),
(4, 'Electric Bike', 15.00, TRUE),
(5, 'Kids Bike', 6.00, TRUE);

-- Insert data into Rentals table
INSERT INTO Rentals (RentalID, BikeID, CustomerName, RentalDurationInHours) VALUES
(1, 1, 'Alice', 3),
(2, 3, 'Bob', 2),
(3, 4, 'Charlie', 5),
(4, 2, 'David', 4),
(5, 5, 'Eva', 1);

-- Insert data into Employees table
INSERT INTO Employees (EmployeeID, EmployeeName, EmployeeRole, Salary) VALUES
(1, 'John', 'Manager', 50000.00),
(2, 'Lisa', 'Sales Associate', 35000.00),
(3, 'Michael', 'Mechanic', 40000.00),
(4, 'Olivia', 'Customer Service', 30000.00),
(5, 'Peter', 'Accountant', 45000.00);

-- Insert data into Services table
INSERT INTO Services (ServiceID, EmployeeID, ServiceType, ServiceCharge) VALUES
(1, 3, 'Repair', 50.00),
(2, 2, 'Consultation', 30.00),
(3, 4, 'Maintenance', 40.00),
(4, 1, 'Training', 60.00),
(5, 5, 'Accounting', 70.00);
