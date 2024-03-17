# complete_adobe_experience_manager_guide
Platform For Adobe Experience Manager




## What is AEM




## Why , What and Latest

   All version of AEM


   Latest version of AEM
   
   
    


## Create a Test Project 
<details><summary><b>info</b></summary>

      - https://experienceleague.adobe.com/en/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/project-archetype/project-setup        

   Step -1 

     - sudo apt install maven  
	  - mvn --version

     - create directory i.e - code 

  Step -2

      - run the below commands


         mvn -B org.apache.maven.plugins:maven-archetype-plugin:3.2.1:generate \
		    -D archetypeGroupId=com.adobe.aem \
		    -D archetypeArtifactId=aem-project-archetype \
		    -D archetypeVersion=39 \
		    -D appTitle="WKND Sites Project" \
		    -D appId="wknd" \
		    -D groupId="com.adobe.aem.guides" \
		    -D artifactId="aem-guides-wknd" \
		    -D package="com.adobe.aem.guides.wknd" \
		    -D version="0.0.1-SNAPSHOT" \
		    -D aemVersion="cloud"


     -  cd aem-guides-wknd 

     - mvn clean install -PautoInstallSinglePackage (this command will push the test project to AEM dashboard)     ---> may build fail due to port issue so change the port in pom.xml file

     - 

</details>

### How to start the AEM Project

<details><summary><b>info</b></summary>

    Way -1 ( direct way)
    -------------------

             - open the terminal from  author and publish  directory then run below command to start the AEM project

                   -  java -jar aem-author-p4052.jar
                   -  java -jar aem-publish-p4053.jar

    Way -2 (start script options)
    -----------------------------

             - codilar@codilar-Latitude-E5470:~/Videos/Learn/author$      = java -jar aem-author-p4052.jar -unpack   -----> unpack the file it will not start it genereate the quickstart files
   
             - change the port inside start file  eg- port 5502
  
             - codilar@codilar-Latitude-E5470:~/Videos/Learn/author/crx-quickstart/bin$ ./start     ----------> start (need to type the port in browser)
     
             - codilar@codilar-Latitude-E5470:~/Videos/Learn/author/crx-quickstart/bin$ ./stop      ----------> stop the application

     
     Way -3 (start by GUI )
    -----------------------
               you must be on author or publish directory 
               
               - codilar@codilar-Latitude-E5470:~/Videos/Learn/author$     =  java jar aem-author-p4052.jar -gui    -----> in this it will help to see the connection window

</details>



## AEM Syllabus
<details><summary><b>info</b></summary>

      Syllabus
      --------
        - Basics of CMS and AEM
        - AEM Installation
        - AEM Environment
        - AEM Consoles
        - AEM Sites/Assets/Authoring
        - Basics of Component and Templates
        - Editable Template and Style System
        - Multisite Manager/ Internalizations/ Language Copy/ Live Copy
        - AEM Concepts and Functionalities
        - Basics of AEM Development and Setup
        - Component Development

</details>

               
## AEM Basic

<details><summary><b>info</b></summary>
	
    AEM Roles
    ---------
              - Author/Marketing/Managers/Non-Development Roles
              
              - QA/QE  -- Quality Assurance
               
              - Developers
              
              - AEM Adminstrators / DevOps


                   
    CMS   
       ----------> AEM installation  --------  AEM Consoles               Development Basics
       ----------> AEM Environments  --------  AEM Authoring  ----------> Development Setup
    AEM                                        AEM Concepts               Component
          
              

    What is CMS
    -----------
            - A CMS helps to create,manage and modify content on a website without the need for specialized technical knowledge
   
     Types of CMS
     ------------
       |
       |-----Traditional CMS----|---- Coupled CMS
       |                        |---- Decoupled CMS
       |
       |-----Headless CMS (only content not rendering functionality)
       |
       |----- Hybrid CMS (headless / traditional -----AEM is Hybrid Decoupled CMS)   ------> headless(content can provide to other system as well form of Json or XML)


    CMS 
    ---
    |
    |---------- Content Management Application
    |
    |---------- Content Delivery Application
    |
    |---------- Front End / Presentation
    
 also 
 
    CMS
     |
     |-------- Content Management System
     |
     |-------- Digital Asset Management
     |
     |-------- User/Permissions Management
     |
     |-------- Headless Feature
     |
     |-------- Build and Run Websites


     What is AEM
     ------------
          - AEM is a comprehensive content management solution for building websites, mobile apps and forms. AEM makes it easy to manage your marketing  content and assets
          - It is a part of adobe cloud (it is enterprise edition)

    Types of AEM
    ------------
      |
      |------------- On-Permises/ Stand Alone(6.5 version) -------------->(local machine or cloud platform we can install)
      |
      |
      |
      |------------- Cloud Based - AEM as a Cloud Service (only installed over cloud through adobe sandbox)
                          |
                          |
                          |-------------- Standalone JAR/ Local (only for local machine)
                          |
                          |-------------- Sandbox
      

    AEM
    ----
       |
       |----------------- Content management System
       |
       |----------------- Digital Asset Management
       |
       |----------------- User/ Permissions Management
       |
       |----------------- Forms Management
       |
       |----------------- Headless Feature
       |
       |----------------- Frontend Tech / Other FE Framework integrations
       |
       |----------------- Servlet/ OSGi Container
       |
       |----------------- Build and Run Websites


    AEM Instances Terminologies
    ----------------------------
 
          - AEM Instance (when we install the AEM)
          
          - Environment / RunModes
          
          - Dispatcher (between enduser and AEM generally we set a webserver 
                        but webserver does not know AEM so we put a tiny module inside the webserver 
                        so that webserver know how to intercat with AEM this tiny module we called as dispatcher)

    Types of Instances
    -------------------
       |
       |
       |---------------- author (create content)
       |
       |
       |---------------- publish / publisher (serve the content to enduser)
       

    Environment and RunModes
    ------------------------
       |
       |---------- dev
       |
       |---------- qa
       |
       |---------- stage
       |
       |---------- prod
       |
       |---------- any name              
   
              - AEM instances can be identify by environment or by  runModes


              
    AEM Environments
    ----------------
 
        - AEM Environment Setup
        
        - AEM Environment Variations 


                  
     
     Author (create content on author instance)
     ------------------------------------------
     |
     |------------ Publish-1         <-------                Webserver(tiny module)                          ---------> serve to end user
     |
     |                                                                                   Load-balancer
     |
     |
     |------------ Publish-2        <--------                Webserver(tiny module)                          ---------> serve to end user



     AEM Sites
     ----------

	      -  overview of dashboard




    Page properties and Page operations
    -----------------------------------

                          Edit / Preview
			   |
                           |------- Layout
			   |------- Developer
                           |------- Timewarp





     - AEM build on JCR (Java Content Repository) to save the Data (now days we can use the MongoDb)


    Editable Templates in AEM  - https://youtu.be/GnTrhSc2Wg0?feature=shared
    -------------------------

           - Create and Edit Editable Template
	   - Structure
           - Initial Content
	   - Policies
           - Layout


	
	       - all the template store under   -- conf  folder 
	
	       - when we create any new template that  are in draft mode with yellow header -- so we need to enable
	
	       - Template and Pages has static relation i.e -- > what ever added in intial content, template and pages  that will be available for new pages but not available for old pages
	       
	       - What ever we add into structure i.e Dynamically binded so (it will append to old or new pages )
	
	       - What ever we add into structure section we can not edit, delete on pages


     Template Creation (Pages) 
     -------------------------
             |
	     |---- Structure
             |---- Initial Content
	     |---- Layout

      
       - Structue(available to all pages & not editable , deletable) and Intial Content (not available to older pages)


    AEM Component (Save Content to JCR or Anywhere)
    -----------------------------------------------
	    - Building block of content creation and content rendering
            - create, save , access 

            Component
	    --------- 
               |
	       |---------- User Content---------------------- Dialog(UI)  ------------- save the content (content store into repository)
	       |---------- Access Content ------------------- Sling Model(Backend) 
	       |---------- Styling -------------------------- clientlibs(create a folder put - font, css, Js and all i.e call - clientlibs)
	       |---------- Rendering ------------------------ Sightly/HTL ----------- 


      Component Cycle
      ---------------
                - Node is Create on JCR(data store in key value pair) when we create a component.
		
		      Dialog -- Authoring Component   |
	                          |                   |  --------------- Authoring
			          |                   |
	                Save Content in Repository    |
            -------------------------------------------------------------------------------------------
	             Sling Model - Access Content for Repository               |                       
	                            |                                          |
			            |                                          |
	              Page Load -- Load clientlibs(CSS/JS)                     |-------------- Rendering
	                            |                                          |
			            |                                          |
	              Slightly Load content from Sling Model in Component      |
	         (Load Data from   - Sling Model and CSS,JS from clientlibs )  |


	       OOTB Component
	       --------------
			  - Foundational Components
	                  - Core Components 	   

   

    AEM Content Policies (Ploicies are define in - Structure Mode not in Initial Mode For Template)
    -----------------------------------------------------------------------------------------------
                 - Content policies are template-level configurations for the templates and its components. 
		 - The content policies define the design properties of a component.
                 - client libary we will be added by page component way

           Content Policies
	   ----------------
                   |
		   |------- Page Level Policy
                   |------- Component Policy


    
    Lock and Unlock Component Structure in AEM (For Template)
    ---------------------------------------------------------
                     - once we lock or unlock we need to correct our strutue bcz it is set to default structure


		     
     What is Clientlibs in AEM - https://youtu.be/bpY3ttLaAi8?feature=shared
     -------------------------
	                   -  To render a page properly we need javascript,css and other resources like (Fonts, Icons) in AEM we store these in specific folder called - cq:ClientLibraryFolder (clientlibs)
	
	                   -  create node of cq:ClientLibraryFolder type to create clientlibs
	
	          Clientlibs Properties
		   ---------------------
	                      - allowProxy --------> allow anonymous user in publish instance
			      - categories
		              - dependencies ------> load this before your clientlibs load
		              - embed        ------> 
	
	          how to declare files
		  ---------------------
	                            #base = css  ---------> folder name
				     style.css  ----------> file name



       Style System in AEM
       -------------------
             - The Style System allows to define style classes in the content policy of a component and page policy of 
	       template so that a content author is able to select them when editing the component on a page.
	
             - These styles can be alternative visual of a component, making the component more flexible.

             - add Style(CSS classes) to Page Policy and Content policy


	         Style System (Template Author & Content Author)
		 -----------------------------------------------
	                 |
			 |---------- Clientlibs(JS,CSS)
	                 |
			 |---------- Style Name to Content/Page Policy
	                 |
			 |---------- Choose Style While Authoring

    
       
      Page Versioning in AEM  - https://youtu.be/OOE4olCjUoI?feature=shared
      -----------------------	
      
     













      

                    

       
     

     


      

   
   
