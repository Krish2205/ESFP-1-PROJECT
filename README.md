# ESFP-1-PROJECT
DRIVING LICENSE CONTROLLED SMART VEHICLE
#include<stdio.h>
#include<string.h>
#include<stdlib.h>
int homepage()
{
	char fname[10];
	char mname[10];
	char lname[10];
	char branch[30];
	char mail[30];
	
	
	printf("\n NAME: KRISH PATEL");
	printf("\n AGE: 18");
	printf("\n VALID UNTIL: 1/1/2035");
}
int main()
{
	char *uid="ADMIN",*psd="12345";
	char id[5],pass[5],a[10],d[10],e[10];
	int len1,len2,c,b;
	char ch;
	FILE *p;
	
	int choice;
	printf("========================================================================================================================");
	printf("\n                                      DRIVING LICENSE CONTROLLEDSMART VEHICLE                                                ");
	printf("\n========================================================================================================================");
	
	printf("\n                                   PRESS <1> FOR ADMIN. ");
	printf("\n                                   PRESS <2> HOW TO IMPROVE ROAD SAFETY IN INDIA. ");
	printf("\n                                   PRESS <3> ROAD SAFETY RULES AND REGULATIONS. ");
	printf("\n                                   PRESS <4> FOR CATEGORIES OF LICENSE. ");
	printf("\n                                   PRESS <5> DOCUMENTS REQUIRED FOR DRIVING LICENSE. ");
	printf("\n                                   ENTER YOUR CHOICE :");
    scanf("%d",&choice);
    
    switch(choice)
    {
    case 1:
    printf("\n         ---------------------------------------------------------------------------------------------------       ");
	printf("\n");
	printf("\n                                                 ADMIN ROOM :                                                 ");
	printf("\n         ---------------------------------------------------------------------------------------------------       ");
	krish:
	printf("\nENTER YOUR ID:");
	scanf("%s",id);
	printf("\nENTER YOUR PASSWORD:");
	scanf("%s",pass);
	
	len1=strcmp(uid,psd);
	len2=strcmp(id,pass);
	
	if(len1==len2)
	{
		homepage();
	}
	else
	{
		printf("YOU HAVE ENTERED WRONG USERNAME OR PASSWORD");
		goto krish;
	}
	printf("\n------------------------------------------------------------------------------------------------------------------------");
	break;
	
	case 2:
		printf("\n------------------------------------------------------------------------------------------------------------------------");
		printf("\n        What steps can be taken to improve Road Safety in India?");
		printf("\n------------------------------------------------------------------------------------------------------------------------");

    		p=fopen("case2.txt","r");
	while((ch=getc(p))!=EOF)
	{
		printf("%c",ch);
	}
	fclose(p);
		break;
		
	case 3:
		p=fopen("case3.txt","r");
	while((ch=getc(p))!=EOF)
	{
		printf("%c",ch);
	}
	fclose(p);
	break;
	
	case 4:
		printf("\n------------------------------------------------------------------------------------------------------------------------");
		printf("\nThis are the types of driving licence in India.");
		printf("\n------------------------------------------------------------------------------------------------------------------------");
	    printf("\n");
	    printf("\n");
		printf("\n1----MC 50CC (Motorcycle 50cc) ??? motorcycles with an engine capacity of up to 50cc.");
		printf("\n2----MC EX50CC (Motorcycle more than 50cc) ??? motorcycles, light motor vehicle, and cars.");
		printf("\n3----Motorcycles/Scooters of any engine capacity, with or without gears with an engine capacity of 50cc or more (old category).");
		printf("\n4----MC Without Gear or M/CYCL.WOG (Motorcycle Without Gear) ??? motorcycles, scooters without gears, all motorcycles.");
		printf("\n5----MCWG or MC With Gear or M/CYCL.WG (Motorcycle With Gear) ??? all motorcycles, engine capacity more than 175cc.");
		printf("\n6----LMV-NT (Light Motor Vehicle???Non Transport) ??? for personal use only.");
		printf("\n7----LMV-INVCRG-NT (Light Motor Vehicle???Invalid Carrige-Non Transport) ??? for personal use by physically handicapped persons only.");
		printf("\n8----LMV-TR (Light Motor Vehicle???Transport) ??? for commercial transportation including light goods carrier.");
		printf("\n9----LMV (Light Motor Vehicle)' ??? including cars, jeeps, taxis, delivery vans.(16th Apr 2018 GOI Ministry of Road Tran & Highways No. RT-11021/44/2017-MVL).");
		printf("\n10---LDRXCV (Loader, Excavator, Hydraulic Equipment) ??? for Commercial application of all hydraulic heavy equipment.");
		printf("\n11---HMV (Heavy Motor Vehicle) ??? a person holding an LMV driving licence can only apply for a heavy licence.");
		printf("\n12---HPMV (Heavy Passenger Motor Vehicle).");
		printf("\n13---HTV Heavy Transport Vehicle (Heavy Goods Motor Vehicle, Heavy Passenger Motor Vehicle).");
		printf("\n14---TRANS (Heavy Goods Motor Vehicle, Heavy Passenger Motor Vehicle).");
		printf("\n15---TRAILR ??? for all kinds of trailers.");
		printf("\n16---AGTLR ??? (Agricultural Tractor and Power Tiller) A person holding an AGTLR can drive an Agricultural tractor and Power tiller on farms, local roads, some Major District Roads and some highways without a trailer. (most of the highways are restricted for farm machinery and slow-moving equipment, some jurisdiction have different rules, so the operator need to go through the concerned Authority).");
		printf("\n17---Additional Endorsement of Driving Licence ??? (AEDL) Private/Commercial drivers should have an additional Badge if they are driving a taxi or any other public transport vehicle.");

		break;
		
	case 5:
		p=fopen("case5.txt","r");
	while((ch=getc(p))!=EOF)
	{
		printf("%c",ch);
	}
	fclose(p);
	break;
	}
	
	
	return 0;
}
