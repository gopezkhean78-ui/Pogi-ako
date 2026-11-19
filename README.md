

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gopez | My Portfolio</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            background: #090510;
            color: white;
            font-family: Arial, sans-serif;
            overflow-x: hidden;
        }

        /* NAVIGATION */
        nav {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 35px;
            padding: 22px 5%;
            background: #110a1c;
            position: sticky;
            top: 0;
            z-index: 100;
            flex-wrap: wrap;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-size: 17px;
            transition: 0.3s;
        }

        nav a:hover {
            color: #bd83ff;
            text-shadow: 0 0 10px #a855f7;
        }

        /* HOME SECTION */
        .home {
            min-height: 750px;
            padding: 80px 6%;
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 50px;
            width: 100%;
        }

        .hero {
            flex: 1;
            max-width: 55%;
        }

        .hero h1 {
            font-size: clamp(40px, 5vw, 65px);
            color: #bd83ff;
            text-shadow: 0 0 20px #a855f7;
            margin-bottom: 20px;
        }

        .hero h2 {
            font-size: 27px;
            margin-bottom: 18px;
        }

        .hero p {
            font-size: 18px;
            line-height: 1.7;
            color: #d8c9e8;
        }

        /* PROFILE PHOTO */
        .profile {
            width: 42%;
            max-width: 520px;
            flex-shrink: 0;
            text-align: center;
        }

        .profile img {
            display: block;
            width: 100%;
            height: 570px;
            object-fit: cover;
            background: #171024;
            border: 4px solid #bd83ff;
            border-radius: 18px;
            box-shadow: 0 0 30px #a855f7;
        }

        .profile p {
            color: white;
            font-size: 21px;
            font-weight: bold;
            margin-top: 18px;
        }

        /* GENERAL SECTIONS */
        section {
            width: 100%;
            padding: 90px 8%;
            text-align: center;
            scroll-margin-top: 80px;
        }

        section h2 {
            font-size: 36px;
            color: #bd83ff;
            margin-bottom: 25px;
            text-shadow: 0 0 15px #a855f7;
        }

        section p {
            font-size: 18px;
            line-height: 1.7;
            color: #d8c9e8;
        }

        /* TASK CARDS */
        .cards {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            align-items: stretch;
            gap: 30px;
            width: 100%;
            margin: 40px auto 0;
        }

        .card {
            flex: 1 1 280px;
            max-width: 350px;
            min-height: 190px;
            padding: 30px;
            background: #171024;
            border: 2px solid #8b4bd1;
            border-radius: 15px;
            box-shadow: 0 0 15px #5b238c;
            transition: 0.3s;
        }

        .card:hover {
            transform: translateY(-8px);
            box-shadow: 0 0 25px #a855f7;
        }

        .card h3 {
            color: #d6aaff;
            margin-bottom: 18px;
            font-size: 21px;
        }

        .card p {
            font-size: 15px;
        }

        /* FOOTER */
        footer {
            width: 100%;
            text-align: center;
            padding: 30px;
            background: #110a1c;
            color: #a98bc5;
        }

        /* TABLET AND MOBILE */
        @media (max-width: 900px) {

            nav {
                gap: 20px;
                padding: 18px 10px;
            }

            nav a {
                font-size: 15px;
            }

            .home {
                min-height: auto;
                padding: 60px 7%;
                flex-direction: column;
                justify-content: center;
                gap: 40px;
            }

            .hero {
                max-width: 100%;
                width: 100%;
                text-align: center;
            }

            .hero h1 {
                font-size: 42px;
            }

            .profile {
                width: 100%;
                max-width: 480px;
            }

            .profile img {
                height: 480px;
            }

            section {
                padding: 65px 6%;
            }

            .cards {
                gap: 20px;
            }

            .card {
                flex: 1 1 280px;
            }
        }

        /* SMALL MOBILE */
        @media (max-width: 480px) {

            nav {
                gap: 14px;
            }

            nav a {
                font-size: 13px;
            }

            .hero h1 {
                font-size: 34px;
            }

            .hero h2 {
                font-size: 22px;
            }

            .hero p {
                font-size: 16px;
            }

            .profile img {
                height: 400px;
            }

            section h2 {
                font-size: 29px;
            }

            section p {
                font-size: 16px;
            }

            .card {
                flex: 1 1 100%;
            }
        }

    </style>
</head>

<body>

    <!-- NAVIGATION -->
    <nav>
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#learning">Learning</a>
        <a href="#midterm">Midterm</a>
        <a href="#final">Final</a>
    </nav>

    <!-- HOME SECTION -->
    <div class="home" id="home">

        <div class="hero">
            <h1>DOMAIN EXPANSION</h1>

            <h2>Welcome to My Portfolio!</h2>

            <p>
                Enter my domain and explore my learning journey,
                laboratory activities, and achievements.
            </p>
        </div>

        <!-- PROFILE PHOTO -->
        <div class="profile">

            <img src="158f0f27-2a6c-42de-9146-f702ac19ffa4.jpg"
                 alt="My Profile Photo">

            <p>Gopez, Khean Aislie S.</p>

        </div>

    </div>

    <!-- ABOUT ME -->
    <section id="about">

        <h2>About Me</h2>

        <p>
            Hello! I am Gopez, Khean Aislie S, an aspiring student
            who wants to become a developer in the future.
            May bitaw pero di matitibag rawr.
        </p>

    </section>

    <!-- LEARNING JOURNEY -->
    <section id="learning">

        <h2>My Learning Journey</h2>

        <p>
            This section contains my experiences, lessons,
            and progress throughout the course.
        </p>

    </section>

    <!-- MIDTERM TASKS -->
    <section id="midterm">

        <h2>Midterm Laboratory Tasks</h2>

        <div class="cards">

            <div class="card">
                <h3>Laboratory Task 1</h3>
                <p>dito ilalagay ang link pero di ko pa nilagay dahil ang hirap ilagay aray mo.</p>
            </div>

            <div class="card">
                <h3>Laboratory Task 2</h3>
                <p>dito ilalagay ang link pero di ko pa nilagay dahil ang hirap ilagay aray mo.</p>
            </div>

            <div class="card">
                <h3>Laboratory Task 3</h3>
                <p>dito ilalagay ang link pero di ko pa nilagay dahil ang hirap ilagay aray mo.</p>
            </div>

        </div>

    </section>

    <!-- FINAL TASKS -->
    <section id="final">

        <h2>Final Laboratory Tasks</h2>

        <div class="cards">

            <div class="card">
                <h3>Final Task 1</h3>
                <p>dito ilalagay ang link pero di ko pa nilagay dahil ang hirap ilagay aray mo.</p>
            </div>

            <div class="card">
                <h3>Final Task 2</h3>
                <p>dito ilalagay ang link pero di ko pa nilagay dahil ang hirap ilagay aray mo.</p>
            </div>

            <div class="card">
                <h3>Final Task 3</h3>
                <p>dito ilalagay ang link pero di ko pa nilagay dahil ang hirap ilagay aray mo.</p>
            </div>

        </div>

    </section>

    <!-- FOOTER -->
    <footer>
        <p>© 2026 Gopez, Khean Aislie S. | Domain Expansion</p>
    </footer>

</body>
</html>
