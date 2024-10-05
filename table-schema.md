# Table

## Table Users
| Field | type | status |
| -------- | ------- | ------- |
| id | int | primary key |
| name | string | |
| username | string | unique |
| password | string | |
| email | string | unique |
| role | string | |

## Table Vehicle
| Field | type | status |
| -------- | ------- | ------- |
| id | int | primary key |
| vehicle | string | |
| bbm_consume | int | |
| status | string | |

## Table Driver
| Field | type | status |
| -------- | ------- | ------- |
| id | int | primary key |
| driver_name | string | |
| status | status | |

## Table Bookings
| Field | type | status |
| -------- | ------- | ------- |
| id | int | primary_key |
| id_vehicle | int | foreign_key - id (Vehicle) |
| id_driver | int | foreign_key - id (Driver) |
| id_approvel | int | foreign_key - id (Users) |
| status | int | |
| destination | string | |
| date | date | |
