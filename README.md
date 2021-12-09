# KANBAN_MASTER
Creating a Warehouse kanban system using ASPNET MVC
This is a wharehouse KANBAN printing system that utilises MSSQL and ASPNET MVC.
System that is current running on is MSSQL Server 2021
MVC that the system being developed on is ASPNET MVC 5.

This system has 3 table which inclused the KANBAN MASTER, SUPERMARKET LINE CAPACITY and the SUPERMARKET ADDRESS

which is created via : 


    CREATE SUPERMARKET SLIDER
    
    
USE [IBusinessTest]
GO

/****** Object:  Table [dbo].[SUPERMARKET_SLIDER]    Script Date: 14/07/2021 12:03:47 PM ******/
SET ANSI_NULLS ON
GO

SET QUOTED_IDENTIFIER ON
GO

CREATE TABLE [dbo].[SUPERMARKET_SLIDER](
	[ID] [int] IDENTITY(1,1) NOT NULL,
	[SLIDER_ADDRESS] [nvarchar](25) NULL,
	[PART_NUMBER] [nvarchar](65) NULL,
	[STATUS] [nvarchar](25) NULL,
	[RACK] [nvarchar](25) NULL,
	[AREA] [nvarchar](30) NULL,
	[BIN] [nvarchar](25) NULL,
	[COLOR] [nvarchar](30) NULL,
	[MULTIPLE_PLART] [bit] NULL
) ON [PRIMARY]
GO


    CREATE KANBAN MASTER
    

USE [IBusinessTest]
GO

/****** Object:  Table [dbo].[KANBAN_MASTER]    Script Date: 14/07/2021 12:04:24 PM ******/
SET ANSI_NULLS ON
GO

SET QUOTED_IDENTIFIER ON
GO

CREATE TABLE [dbo].[KANBAN_MASTER](
	[ID] [int] IDENTITY(1,1) NOT NULL,
	[PHOTO] [image] NULL,
	[PART_NO] [nvarchar](20) NULL,
	[PART_NAME] [text] NULL,
	[MODEL] [nvarchar](25) NULL,
	[LINE] [text] NULL,
	[OUTPUT] [int] NULL,
	[USAGE] [int] NULL,
	[PROCESS] [nvarchar](10) NULL,
	[QTY_PER_TRAY] [int] NULL,
	[TARY_PER_BIN] [int] NULL,
	[QTY_PER_BIN] [int] NULL,
	[BIN_TYPE] [nvarchar](5) NULL,
	[LOCATION] [nvarchar](20) NULL,
	[SLIDER_ADDRESS] [text] NULL,
	[KITTING_SLIDER] [nvarchar](5) NULL,
	[STORE_KANBAN_QTY] [int] NULL,
	[PROD_KANBAN_QTY] [int] NULL,
	[BASIC_FINISH_DATE] [date] NULL,
	[REVISION] [text] NULL,
	[BIN_NUMBER_END] [nvarchar](10) NULL,
	[CYCLE_TIME] [int] NULL,
	[SUPPLIER] [nvarchar](40) NULL,
	[REMARKS] [text] NULL
) ON [PRIMARY] TEXTIMAGE_ON [PRIMARY]
GO

CREATE SUPERMARKET LINE CAPACITY 

USE [IBusinessTest]
GO

/****** Object:  Table [dbo].[SUPERMARKET_LINE_CAPACITY]    Script Date: 09/12/2021 8:14:00 AM ******/
SET ANSI_NULLS ON
GO

SET QUOTED_IDENTIFIER ON
GO

CREATE TABLE [dbo].[SUPERMARKET_LINE_CAPACITY](
	[ID] [int] IDENTITY(1,1) NOT NULL,
	[CUSTOMER] [nvarchar](15) NULL,
	[H0] [nvarchar](4) NULL,
	[A0] [nvarchar](4) NULL,
	[MODEL] [nvarchar](70) NULL,
	[CAPACITY] [int] NULL,
	[MINUTE_30] [int] NULL,
	[MINUTE_60] [int] NULL,
	[MINUTE_90] [int] NULL
) ON [PRIMARY]
GO


