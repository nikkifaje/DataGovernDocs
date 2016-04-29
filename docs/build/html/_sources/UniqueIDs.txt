Unique IDs
------------



========	===================	==============================================================================	======================================================================================================	======	===========	=====	=======	========================= =============	=========== ==================	=========
UniqueID	Item			UnitDefinition									SQLDescription												Owner	Department	Type	Origin	Destination		  DateAdded	Population  Population Missing	PrtClean
========	===================	==============================================================================	======================================================================================================	======	===========	=====	=======	========================= =============	=========== ==================	=========
103		NoApprovalCode		Shows who approved the loan; helps to track underwriters			APPROVALCODE = 0											NULL	Lending		Loan	DLC	SymitarExtracts.dbo.LOAN  1/1/2016 0:00	NULL	    NULL		NULL
104		CreditLimitExpLOC	LOC with no balance, credit limit, and credit limit expiration day < present	TYPE BETWEEN 5000 AND 5004  AND BALANCE = 0 AND CREDITLIMIT = 0 AND CREDLIMITEXPIRATION < GETDATE()	NULL	Lending		Loan	DLC	SymitarExtracts.dbo.LOAN  1/1/2016 0:00	NULL	    NULL		NULL
105		CreditLimitExpOther	Loans with no balance, credit limit, and credit limit expiration day < present	TYPE NOT BETWEEN 5000 AND 5004 AND BALANCE = 0 AND CREDITLIMIT = 0 AND CREDLIMITEXPIRATION < GETDATE()	NULL	Lending		Loan	DLC	SymitarExtracts.dbo.LOAN  1/1/2016 0:00	NULL	    NULL		NULL
106		MissingOrgFICO		No FICO was recorded during loan organization					BUREAUSCORE1 = 0 AND (a.TYPE not between 6000 and 6500)							NULL	Lending		Loan	DLC	SymitarExtracts.dbo.LOAN  1/1/2016 0:00	NULL	    NULL		NULL
107		NoLoanOpenDate		No Open Date was recorded during loan organization				OPENDATE IS NULL											NULL	Lending		Loan	DLC	SymitarExtracts.dbo.LOAN  1/1/2016 0:00	NULL	    NULL		NULL
========	===================	==============================================================================	======================================================================================================	======	===========	=====	=======	========================= =============	=========== ==================	=========