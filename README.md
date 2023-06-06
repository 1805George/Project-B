# Project-B
<!-----------------index.html sheet----------------->
Note: at Lines: 18-20, there's a Javascript functions meant for small screan responsive views, while from lines 27 to 28, there's Bar-Menu for the same small-screen view. The main body of the javascript functions are from lines 43 to 49. Take note also that the final sections and divisions of the page are yet to be made. 
<!DOCTYPE html>
<html>
    <head>
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title> Multi_Mode Student's Hostel Booking & Accommodation System</title>
        <link rel="stylesheet" href="style.css">
        <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
    </head>
<body>
    <section class="header">
        <nav>
            <a href="index.html">
                <img class="Logo-image" src="images/Hostels Logo.jpg"></a>

            <div class="nav-links" id="navLinks">
                <i class="fa fa-times" onclick="hideMenu()"></i>
                <ul>
                    <li><a href="">HOME</a></li>
                    <li><a href="">SERVICES</a></li>
                    <li><a href="">CONTACT US</a></li>
                    <li><a href="">CUSTOMER CARE</a></li>
                </ul>
            </div>
            <i class="fa fa-bars" onclick="showMenu()"></i>
        </nav>
     <div class="text-box">
        <h1>Multi-Mode Hostels & Accomodation</h1>
        <p>Students all over Kenya doesn't have to worry now as hostel's 
            acquisition and bookings is now made easy and simple. <br>All 
            you've got to do is visit our webapp page from the conformt
            of you seat, locate the hostels over the map, book, and pay.
            <br>Move in any time you'd want, provided payments have been processed.
        </p>
        <a href="" class="hero-btn">Visit us to know More</a>
     </div> 
    </section>

<!-----JavaScript for Toggle Menu Response With a Variable and a Function----->
    <script>
    var navLinks = document.getElementById("navLinks");
        function showMenu(){
        navLinks.style.right = "0";
        }
    function hideMenu(){
        navLinks.style.right = "-200px";
    }
    </script>
<!-----New Section: "Rooms/Hostels we offer"----->
<section class="Rooms">
    <h1> Rooms Available with Us </h1>
    <p>Quality with Affordability</p>
<!---3 Columns Content on the section with immediate description--->
    <div class="row">
        <div class="Rooms-col">
            <h3>County-based</h3>
            <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit.Ex itaque, modi doloremque cumque alias illo rem dolores error deserunt <br>accusantium quos vero velit inventore est possimus, <br>quae ipsa atque voluptas.</p>
        </div>
        <div class="Rooms-col">
            <h3>Region-based</h3>
            <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit.Ex itaque, modi doloremque cumque alias illo rem dolores error deserunt <br>accusantium quos vero velit inventore est possimus, <br>quae ipsa atque voluptas.</p>
        </div>
        <div class="Rooms-col">
            <h3>School-based</h3>
            <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit.Ex itaque, modi doloremque cumque alias illo rem dolores error deserunt <br>accusantium quos vero velit inventore est possimus, <br>quae ipsa atque voluptas.</p>
        </div>
    </div>
    </section>
</body>


<!----------CSS Section-------------->
  *{
    margin: 0;
    padding: 0;
    font-family: sans-serif;

}
.header{
    min-height: 100vh;
    width: 100%;
    background-image:url(images/background3.jpg);
    background-position: center;
    background-size: cover;
    position: relative;
}
nav{
    display:flex;
    padding: 2% 2%;
    justify-content: space-between;
    align-items: center;
}
nav img{
    width: 80px;
}
.nav-links{
    flex: 1;
    text-align: right;
}
.nav-links ul li{
    list-style: none;
    display: inline-block;
    padding: 4px 4px;
    position: relative;
    text-decoration-color: rgb(83, 6, 132);
}
/*Navigation Menu (Home,Services,Contacts...*/
.nav-links ul li a{
    color: #fefcfb;
    text-decoration: none;
    font-size: 16px;
    font-weight: bolder;
}

/*Underlines of the Menu Items*/
 .nav-links ul li::after{ 
    content: '';
    width: 100%;
    height: 2px;
    background: #e7c20e;
    display: block;
    margin: auto;
    transition: 0.5s;
}
/*Hover effect of the underlines in the Navigational Menu*/
.nav-links ul li:hover::after{
    width: 0;
}
/*Text box with Web-Intro*/
.text-box{
    font-size: 18px;
    width: 90%;
    color: #ebd72b;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
    text-align: center;
}
/*Styles for Header1*/
.text-box h1{
    font-size: 55px;
}
/* styles for Paragraph*/
.text-box p{
    margin: 10px 0 40px;
    font-size: 16px;
    color: #e2c42c;
}
/*Hero Button Positioning, text-styling*/
.hero-btn{
    display: inline-block;
    text-decoration: none;
    color:white;
    border: 1px solid #fff;
    padding: 12px 34px;
    font-size: 13px;
    background: transparent;
    position: relative;
    cursor: pointer;
}
/*Hero-buton styles*/
.hero-btn:hover{
    border: 1px solid #f44336;
    background: #f44336;
    transition: 1s;
}
/*Styles for the Logo Image*/
.Logo-image{
    width: 50px;
    height: 50px;
    border-radius: 50%;
    overflow: hidden;
}
/*This part hides the Menu & X buttons from the wide screen, only to be visible over the small screen*/
nav .fa{
    display: none;
}

/*Media Query for screen sizes in small devices. Font size should be lower than one used in text-box h1*/
@media(max-width: 700px){
    .text-box h1{
        font-size: 20px;
    }
    .nav-links ul li{
        display: block;
    }
    /*This section creates a pup-up menu for small screen devices: Phones&Tablets*/
    .nav-links {
        position:absolute;
        background: #7d5407;
        height: 100vh;
        width: 200px;
        top: 0;
        right: -200px;
        text-align: left;
        z-index: 2;
        transition: 0.5s;
    }
    /*styles for the close button to reapper while in small screen*/
    nav .fa{
        display: block;
        color: #fff;
        margin: 10px;
        font-size: 18;
        cursor: pointer;
    }
    .nav-links ul{
        padding: 20%; 
    } 
}
/*New Section Rooms*/
/*Formating the Class-Rooms*/
.rooms{
    width: 80px;
    margin: auto;
    text-align: center;
    padding-top: 100px;
    }
/*Formating the Header1 Texts*/
    h1{
    font-size: 36;
    font-weight: 600;
    text-align: center;
   
}
/*Formating the Paragraphs*/
    p{
    color: #777;
    font-size: 14;
    font-weight: 300;
    line-height: 22px;
    padding: 10px;
    text-align: center;
    }
/*The row-column effects*/
.row{
    margin-top: 5%;
    display: flex;
    justify-content: space-between;
}
/*Effecting the columns i.e color, size and fonts*/
.Rooms-col{
    flex-basis:30% ;
    background:#fff3f3;
    border-radius: 10px;
    margin-bottom: 5%;
    padding: 20px 15px;
    box-sizing: border-box;
    transition: 0.5s;
    display: block;
}
/*Header 3 formating*/
    h3{
        text-align: center;
        font-weight: 600;
        font-weight: bolder;
        margin: 10px;
    }
/*Colum Hover Effects*/

.Rooms-col:hover {
    box-shadow: 0 0 20px 0px rgba(0, 0, 0, 0.2);
  }
  
</html>
