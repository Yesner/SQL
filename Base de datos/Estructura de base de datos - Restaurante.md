# Estructura de base de datos - Restaurante

## Tabla Customers

CREATE TABLE "Customers" (
	"CustomerID"	INTEGER,
	"FirstName"	TEXT,
	"LastName"	TEXT,
	"Email"	TEXT,
	"Address"	TEXT,
	"City"	TEXT,
	"State"	TEXT,
	"Phone"	TEXT,
	"Birthday"	TEXT,
	"FavoriteDish"	INTEGER,
	PRIMARY KEY("CustomerID")
)


## Tabla CustomersDishes

CREATE TABLE "CustomersDishes" (
	"CustomersDishesID"	INTEGER,
	"CustomerID"	INTEGER,
	"DishID"	INTEGER,
	PRIMARY KEY("CustomersDishesID")
)

## Tabla CustomersEvents

CREATE TABLE "CustomersEvents" (
	"CustomersEventsID"	INTEGER,
	"CustomerID"	INTEGER,
	"EventID"	INTEGER,
	PRIMARY KEY("CustomersEventsID")
)

## Tabla Dishes

CREATE TABLE "Dishes" (
	"DishID"	INTEGER,
	"Name"	TEXT,
	"Description"	TEXT,
	"Price"	REAL,
	"Type"	TEXT,
	PRIMARY KEY("DishID")
)

## Tabla Events

CREATE TABLE "Events" (
	"EventID"	INTEGER,
	"Name"	TEXT,
	"Description"	TEXT,
	"Date"	TEXT,
	"Location"	TEXT,
	PRIMARY KEY("EventID")
)

## Tabla Orders

CREATE TABLE "Orders" (
	"OrderID"	INTEGER,
	"CustomerID"	INTEGER,
	"OrderDate"	TEXT,
	PRIMARY KEY("OrderID")
)

## Tabla OrdersDishes

CREATE TABLE "OrdersDishes" (
	"OrdersDishesID"	INTEGER,
	"OrderID"	INTEGER,
	"DishID"	INTEGER,
	PRIMARY KEY("OrdersDishesID")
)

## Tabla Reservations

CREATE TABLE "Reservations" (
	"ReservationID"	INTEGER,
	"CustomerID"	INTEGER,
	"Date"	TEXT,
	"PartySize"	INTEGER,
	PRIMARY KEY("ReservationID")
)
