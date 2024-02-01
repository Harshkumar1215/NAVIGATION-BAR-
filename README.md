# NAVIGATION-BAR-
Responsive navigation bar . 
code 
HTML 

 <!-- navigation bar -->
   <!--YOU  can change  the link for own use --> 	
	 
    <nav>
        <!-- for desktop-->
        <ul>
            <li >
                <a href="https://github.com/Harshkumar1215" >HARSH KUMAR </a>
            </li>
            <li class="hide">
                <a href="https://github.com/Harshkumar1215">Home</a>
            </li>
            <li class="hide">
                <a href="https://github.com/Harshkumar1215">About</a>
            </li>
            <li class="hide">
                <a href="#">Contact</a>
            </li>
            <li class="hide">
                <a href="addmissionForm.html">Admission</a>
            </li>
            <li class="hide">
                <a href="courses.html">Courses</a>
            </li>
            <li class="hide">
                <a href="enquiry.html">Enquiry</a>
            </li>
            <li class="hide">
                <a href="#">Login</a>
            </li>
            <li class="menu-button" onclick="showSidebar()">
                <a href="#">≡</a>
            </li>
        </ul>

         <!-- for sidebar-->
         <ul class="sidebar">
            <li onclick="hideSidebar()">
                <a href="#">✖</a>
            </li>
            <li>
                <a href="https://github.com/Harshkumar1215">Home</a>
            </li>
            <li>
                <a href="#">About</a>
            </li>
            <li>
                <a href="#">Contact</a>
            </li>
            <li>
                <a href="addmissionForm.html">Admission</a>
            </li>
            <li >
                <a href="courses.html">Courses</a>
            </li>
            <li>
                <a href="enquiry.html">Enquiry</a>
            </li>
            <li>
                <a href="#">Login</a>
            </li>
        </ul>
JS CODE 

                  <!--show sidebar script-->
              <script>
                  function showSidebar()
                {
                const sidebar = document.querySelector('.sidebar');
                sidebar.style.display = 'flex';
                        }

            function hideSidebar(){
                const sidebar = document.querySelector('.sidebar');
                sidebar.style.display = 'none';
            }
        </script>
    </nav>
.CSS CODE  

       /* navigation bar*/
     nav{ position: fixed;
    background-color:#666;
    box-shadow: 3px 3px 5px rgba(0, 0, 0.1);
    width: 100%;
    

     }
       nav ul{
    width: 100%;
    list-style: none;
    display: flex;
    justify-content: flex-end;
    align-items: center;
    }
     nav li{
    height: 50px;
       }
      nav a{
    height: 100%;
    padding: 0 30px;
    text-decoration: none;
    display: flex;
    align-items: center;
    color: white;
       }
       nav a:hover{
    background-color: aquamarine;
    color: brown;
    border: 15%;
       }      
      nav li:first-child{
    margin-right: auto;
      }

      /*side bar */
      .sidebar{
    position: fixed;
    top: 0;
    right: 0;
    
    height: 50vh;
    width: 200px;
    z-index: 999;
    background-color: rgba(255, 255, 255, 0);
    backdrop-filter: blur(10px);
    box-shadow:-10px 0 5px rgb(122, 116, 116);
    
    display: none;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    }
      .sidebar li{
    width: 100%;
     }
     .sidebar a{
    width: 100%;
     }
      .menu-button{
    display: none;
      }
     @media(max-width: 952px)
      {
    .hide{
        display: none;
    }
    .menu-button{
        display: block;
    }
     }
