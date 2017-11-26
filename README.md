
For detailed information please visit https://radonrad.com/java-easy-licence



# JEL-MANAGER
Java Easy License Manager


#Java Software Product Licensing:
##API, License Manager and Server
JEL provides solutions for Java software product licensing and protection. It includes Java API, JEL-Manager GUI tool, Auto License Generation and Activation Server application and Floating License Server for generation and validation of license text, license key, and floating license file.
JEL is designed to be easy to use and integrate in any Java software application. A small pure Java runtime library provides static methods for license validation, online activation, deactivation and validation. JEL- Manager provides wizard dialogs for generating licenses and license templates.
###JEL-Manager provides Customer/Product/License database where you can follow up your licences and their status.
###JEL-Manager allos you to create/edit/change licenses.
![Alt text](https://radonrad.com/wp-content/uploads/2017/11/baslangic_resmi.png "JEL_MANAGER")

#Step by Step Guide
1. Download or Clone This REPO.
2. Run JEL-MANAGER.jar (sqlite database file should be in the same folder as jel-manager)
```Java
java -jar JEL_MANAGER.jar
```

3. Create a CUSTOMER !
  - Click on Customers tab
  - Enter credientals of the customer on the right hand side panel
  - Click Save (in order to edit. click on the custoemr from the list.)
  ![Alt text](https://radonrad.com/wp-content/uploads/2017/11/customer_create.png "Create Customer")
  
  
4. Create a PRODUCT
  - Click on the Products Tab
  - Enter Product Details on the right hand side panel
  - Click Save(in order to edit, click on the product from the list.)
![Alt text](https://radonrad.com/wp-content/uploads/2017/11/product_create.png "Create Product")


5. Create a Licence
  - Click on the Licences Tab
  - Enter Licence information
  - Choose a customer from dropdown
  - Choose a product from dropdown
  - Choose Start/end data if necesarry
  - Enter MAC ID in format of xx:xx:xx:xx:xx:xx
  - Enter HWID(CHECK THE HWID GATHERING TOOL FOR DETAILS ABOUT HOW TO GET THIS CODE)
  - Enter HS_CODEor Extra_Code if you wish to store extra information on the license.
  - Click SAVE(in order to edit click on the licence from the list)
  ![Alt text](https://radonrad.com/wp-content/uploads/2017/11/license_create.png "Licence Create")
  
  
6. Downloading license file or jars
  - Click on the Summary Tab
  - click on the license you wish to download from the list
  - follow popup.
  ![Alt text](https://radonrad.com/wp-content/uploads/2017/11/popup.png "licence file & jars")


#Advanced
you can change Public Private key pairs for every license you create. In order to do that. you should create public private key pairs via command line and then copy them to application folder. Pleause use the below codes to crete public private key pair.
```
 openssl genrsa -out privkey.pem 2048
 openssl pkcs8 -topk8 -in privkey.pem -inform PEM -nocrypt -outform DER -out privkey.der
 ```
 
Extract the public key, fur publishing.
```
 openssl rsa -in privkey.pem -out pubkey.der -pubout -outform DER
```







# JEL LIBRARY
Java Easy License Library
Main Applications and everything resides in https://github.com/hasansarman/jel
Use JEL_LIBRARY.JAR File to implement and read licence files in your applications.
Download Jar and helper.


Add JEL_LIBRARY.jar to Build Path and then call the function below to check licence.
You can also use Jel_Helper.java to implement functionality.
```Java
String licence_path="licence.jel";
Jel_Helper jel=new Jel_Helper();


 // FOR EASY FAST CHECHING FOR MAC OR HW ID.
if(jel.Check_Licence(licence_path)){
  System.out.println("LICENCE OK !!");
}


//IF YOU ENTERED HS_CODE OR EXTRA CODE THEN YOU SHOULD PASS THIS VLAUES TO Check_Licence(String,String); function
if(jel.Check_Licence(licence_path,HS_CODE,EXTRA_CODE)){
  System.out.println("LICENCE OK !!");
}

License l=jel.get_License();
//INFORMATION CHECK
String s="";
  s+="####Customer Info####\n";
	    //customer name
	    s+="C_NAME -> "+(l.C_NAME==null?"":l.C_NAME)+"\n";
	    s+="C_ADDRESS -> "+(l.C_ADDRESS==null?"":l.C_ADDRESS)+"\n";
	    s+="C_TYPE  ->  "+l.C_TYPE+"\n";
	    s+="C_EMAIL -> "+(l.C_EMAIL==null?"":l.C_EMAIL)+"\n";
	    s+="C_PHONE -> "+(l.C_PHONE==null?"":l.C_PHONE)+"\n";
	    s+="C_COUNTRY -> "+(l.C_COUNTRY==null?"":l.C_COUNTRY)+"\n";
	    s+="C_CITY -> "+(l.C_CITY==null?"":l.C_CITY)+"\n";
	    s+="C_ZIPCODE  ->  "+l.C_ZIPCODE+"\n";
	    
	    
	    s+="C_MOBILE -> "+(l.C_MOBILE==null?"":l.C_MOBILE)+"\n";
	    s+="C_EXTRA_FIELD -> "+(l.C_EXTRA_FIELD==null?"":l.C_EXTRA_FIELD)+"\n";
	    s+="C_ORIGIN -> "+(l.C_ORIGIN==null?"":l.C_ORIGIN)+"\n";
	    
	    
	    s+="####Product Info####\n";
	    s+="P_PRODUCT_ID  ->  "+l.P_PRODUCT_ID+"\n";
	    s+="P_PRODUCT_NAME -> "+(l.P_PRODUCT_NAME==null?"":l.P_PRODUCT_NAME)+"\n";
	    s+="P_PRODUCT_WEBPAGE -> "+(l.P_PRODUCT_WEBPAGE==null?"":l.P_PRODUCT_WEBPAGE)+"\n";
	    s+="P_PRODUCT_HS_CODE -> "+(l.P_PRODUCT_HS_CODE==null?"":l.P_PRODUCT_HS_CODE)+"\n";
	   
	    
	    
```


##DO NOT SEND PRIVATE PUBLIC KEYS wiTH LIBRARY !!
##DO NOT SEND PUB PRIV KEYS TO THE CUSTOMER !!


## Attention WEB BASED ACTIVATION and LICENSE BLOCKAGE VIA SERVER IS NOT ACTIVATED.
## These will be availiable in PRO.This version will always be FREE !!!

 ![Alt text](https://radonrad.com/wp-content/uploads/2017/11/license_activation.png "activation")



