# joellebeau
portfolio
# 👋 Bonjour, moi c’est Joel

<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <meta name="description"
          content="Portfolio de Joel Guei - Réseaux, Cybersécurité, IoT et SOC">

    <title>Joel Guei | Réseaux & Cybersécurité</title>

    <style>

        /* =========================
           VARIABLES
        ========================== */

        :root {
            --bg: #f7f8fa;
            --white: #ffffff;
            --text: #111827;
            --muted: #64748b;
            --border: #e5e7eb;
            --blue: #2563eb;
            --dark: #0f172a;
            --light-blue: #eff6ff;
        }


        /* =========================
           RESET
        ========================== */

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: Arial, Helvetica, sans-serif;
            background: var(--bg);
            color: var(--text);
            line-height: 1.6;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        .container {
            width: min(1120px, 92%);
            margin: auto;
        }


        /* =========================
           NAVBAR
        ========================== */

        nav {
            position: sticky;
            top: 0;
            z-index: 1000;

            background: rgba(255, 255, 255, 0.92);
            backdrop-filter: blur(12px);

            border-bottom: 1px solid var(--border);
        }

        .nav-container {
            height: 70px;

            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .logo {
            font-size: 22px;
            font-weight: 800;
        }

        .logo span {
            color: var(--blue);
        }

        .nav-links {
            display: flex;
            gap: 28px;
            list-style: none;
        }

        .nav-links a {
            font-size: 14px;
            color: #475569;
            transition: 0.3s;
        }

        .nav-links a:hover {
            color: var(--blue);
        }


        /* =========================
           HERO
        ========================== */

        .hero {
            min-height: 90vh;

            display: flex;
            align-items: center;

            background:
                linear-gradient(
                    180deg,
                    #ffffff 0%,
                    #f7f8fa 100%
                );
        }

        .hero-grid {
            display: grid;
            grid-template-columns: 1.3fr 0.7fr;

            gap: 60px;

            align-items: center;
        }

        .badge {
            display: inline-block;

            padding: 7px 14px;

            background: var(--light-blue);
            color: var(--blue);

            border: 1px solid #bfdbfe;

            border-radius: 50px;

            font-size: 13px;
            font-weight: bold;

            margin-bottom: 25px;
        }

        .hero h1 {
            font-size: clamp(42px, 6vw, 75px);

            line-height: 1.05;

            letter-spacing: -3px;

            margin-bottom: 25px;
        }

        .hero h1 span {
            color: var(--blue);
        }

        .hero-description {
            color: var(--muted);

            font-size: 19px;

            max-width: 700px;
        }

        .buttons {
            display: flex;

            gap: 14px;

            margin-top: 30px;

            flex-wrap: wrap;
        }

        .btn {
            display: inline-block;

            padding: 12px 20px;

            border-radius: 12px;

            font-weight: bold;

            border: 1px solid var(--border);

            background: white;

            transition: 0.3s;
        }

        .btn:hover {
            transform: translateY(-3px);
        }

        .btn-primary {
            background: var(--blue);
            color: white;

            border-color: var(--blue);
        }


        /* =========================
           PROFILE CARD
        ========================== */

        .profile-card {
            background: white;

            border: 1px solid var(--border);

            border-radius: 24px;

            padding: 30px;

            box-shadow:
                0 20px 50px rgba(15, 23, 42, 0.08);
        }

        .avatar {
            width: 115px;
            height: 115px;

            display: grid;
            place-items: center;

            background: var(--light-blue);

            color: var(--blue);

            border-radius: 50%;

            font-size: 40px;

            font-weight: 900;

            margin-bottom: 20px;
        }

        .profile-card h2 {
            font-size: 25px;
        }

        .profile-card p {
            color: var(--muted);
        }

        .stats {
            display: grid;

            grid-template-columns: repeat(3, 1fr);

            gap: 10px;

            margin-top: 25px;
        }

        .stat {
            background: #f8fafc;

            padding: 15px;

            border-radius: 14px;

            text-align: center;
        }

        .stat strong {
            display: block;

            font-size: 20px;
        }

        .stat span {
            font-size: 12px;

            color: var(--muted);
        }


        /* =========================
           SECTIONS
        ========================== */

        section {
            padding: 90px 0;
        }

        .section-header {
            margin-bottom: 40px;
        }

        .section-label {
            color: var(--blue);

            text-transform: uppercase;

            letter-spacing: 2px;

            font-size: 12px;

            font-weight: bold;
        }

        .section-header h2 {
            font-size: 40px;

            letter-spacing: -1.5px;

            margin-top: 8px;
        }

        .section-header p {
            color: var(--muted);

            max-width: 700px;

            margin-top: 10px;
        }


        /* =========================
           ABOUT
        ========================== */

        .about-grid {
            display: grid;

            grid-template-columns: 1fr 1fr;

            gap: 25px;
        }

        .card {
            background: white;

            border: 1px solid var(--border);

            border-radius: 22px;

            padding: 28px;

            box-shadow:
                0 10px 30px rgba(15, 23, 42, 0.04);
        }

        .card h3 {
            margin-bottom: 12px;

            font-size: 22px;
        }

        .card p {
            color: var(--muted);
        }


        /* =========================
           SKILLS
        ========================== */

        .skills-grid {
            display: grid;

            grid-template-columns: repeat(3, 1fr);

            gap: 18px;
        }

        .tags {
            display: flex;

            flex-wrap: wrap;

            gap: 8px;
        }

        .tag {
            background: #f1f5f9;

            color: #334155;

            padding: 6px 10px;

            border-radius: 8px;

            font-size: 13px;
        }


        /* =========================
           PROJECTS
        ========================== */

        .projects-grid {
            display: grid;

            grid-template-columns: repeat(2, 1fr);

            gap: 20px;
        }

        .project {
            display: flex;

            flex-direction: column;
        }

        .project-number {
            color: var(--blue);

            font-size: 13px;

            font-weight: 800;
        }

        .project h3 {
            font-size: 23px;

            margin: 8px 0;
        }

        .project p {
            color: var(--muted);
        }

        .project .tags {
            margin: 18px 0;
        }

        .project-link {
            color: var(--blue);

            font-weight: bold;

            margin-top: auto;
        }


        /* =========================
           ROADMAP
        ========================== */

        .roadmap {
            display: grid;

            grid-template-columns: repeat(4, 1fr);

            gap: 15px;
        }

        .roadmap-item {
            background: white;

            border: 1px solid var(--border);

            padding: 22px;

            border-radius: 18px;
        }

        .roadmap-number {
            color: var(--blue);

            font-weight: bold;
        }

        .roadmap-item h3 {
            margin: 7px 0;
        }

        .roadmap-item p {
            color: var(--muted);

            font-size: 14px;
        }


        /* =========================
           CONTACT
        ========================== */

        .contact-box {
            background: var(--dark);

            color: white;

            border-radius: 30px;

            padding: 55px;
        }

        .contact-box h2 {
            font-size: 40px;
        }

        .contact-box p {
            color: #cbd5e1;

            max-width: 650px;

            margin: 12px 0 25px;
        }

        .contact-box .btn {
            background: white;

            color: var(--dark);
        }


        /* =========================
           FOOTER
        ========================== */

        footer {
            text-align: center;

            padding: 35px;

            color: var(--muted);

            font-size: 14px;
        }


        /* =========================
           RESPONSIVE
        ========================== */

        @media (max-width: 850px) {

            .hero-grid {
                grid-template-columns: 1fr;
            }

            .about-grid {
                grid-template-columns: 1fr;
            }

            .skills-grid {
                grid-template-columns: 1fr 1fr;
            }

            .roadmap {
                grid-template-columns: 1fr 1fr;
            }

            .projects-grid {
                grid-template-columns: 1fr;
            }

            .nav-links {
                display: none;
            }

        }


        @media (max-width: 550px) {

            .skills-grid {
                grid-template-columns: 1fr;
            }

            .roadmap {
                grid-template-columns: 1fr;
            }

            .hero h1 {
                font-size: 45px;
            }

            .contact-box {
                padding: 30px 22px;
            }

            .contact-box h2 {
                font-size: 30px;
            }

        }

    </style>
</head>


<body>


<!-- =========================
     NAVIGATION
========================== -->

<nav>

    <div class="container nav-container">

        <a href="#accueil" class="logo">
            Joel<span>.</span>
        </a>

        <ul class="nav-links">

            <li>
                <a href="#apropos">À propos</a>
            </li>

            <li>
                <a href="#competences">Compétences</a>
            </li>

            <li>
                <a href="#projets">Projets</a>
            </li>

            <li>
                <a href="#parcours">Parcours</a>
            </li>

            <li>
                <a href="#contact">Contact</a>
            </li>

        </ul>

    </div>

</nav>



<!-- =========================
     HERO
========================== -->

<header class="hero" id="accueil">

    <div class="container hero-grid">


        <div>

            <div class="badge">
                Disponible pour projets & collaborations
            </div>


            <h1>
                Je sécurise les
                <span>réseaux</span>
                et les infrastructures numériques.
            </h1>


            <p class="hero-description">

                Je suis <strong>Joel Guei</strong>,
                étudiant en Licence 3 Réseaux & Sécurité Informatique,
                passionné par la cybersécurité, l'administration réseau,
                l'IoT et la détection des menaces.

            </p>


            <div class="buttons">

                <a
                    href="#projets"
                    class="btn btn-primary">
                    Voir mes projets
                </a>

                <a
                    href="#contact"
                    class="btn">
                    Me contacter
                </a>

            </div>

        </div>



        <!-- CARTE PROFIL -->

        <div class="profile-card">

            <div class="avatar">
                JG
            </div>

            <h2>
                Joel Guei
            </h2>

            <p>
                Réseaux & Sécurité Informatique
            </p>


            <div class="stats">

                <div class="stat">
                    <strong>L3</strong>
                    <span>Formation</span>
                </div>

                <div class="stat">
                    <strong>4+</strong>
                    <span>Projets</span>
                </div>

                <div class="stat">
                    <strong>SOC</strong>
                    <span>Objectif</span>
                </div>

            </div>

        </div>

    </div>

</header>



<!-- =========================
     A PROPOS
========================== -->

<section id="apropos">

    <div class="container">

        <div class="section-header">

            <div class="section-label">
                Profil
            </div>

            <h2>
                À propos de moi
            </h2>

            <p>
                Comprendre, construire, sécuriser,
                tester et améliorer.
            </p>

        </div>


        <div class="about-grid">


            <div class="card">

                <h3>
                    🎓 Mon parcours
                </h3>

                <p>

                    Je suis étudiant en
                    <strong>
                        Licence 3 Réseaux et Sécurité Informatique
                    </strong>.

                    Je développe mes compétences grâce
                    à des laboratoires Cisco, des architectures
                    réseau, des projets IoT et des travaux pratiques
                    en cybersécurité.

                </p>

            </div>


            <div class="card">

                <h3>
                    🎯 Mon objectif
                </h3>

                <p>

                    Construire un profil professionnel orienté
                    <strong>Analyste SOC</strong> et
                    <strong>Administrateur Réseau & Sécurité</strong>,
                    puis évoluer progressivement vers
                    l'expertise en cybersécurité.

                </p>

            </div>


        </div>

    </div>

</section>



<!-- =========================
     COMPETENCES
========================== -->

<section id="competences">

    <div class="container">

        <div class="section-header">

            <div class="section-label">
                Expertise
            </div>

            <h2>
                Compétences techniques
            </h2>

        </div>


        <div class="skills-grid">


            <!-- RESEAUX -->

            <div class="card">

                <h3>
                    🌐 Réseaux
                </h3>

                <div class="tags">

                    <span class="tag">IPv4 / IPv6</span>

                    <span class="tag">VLAN</span>

                    <span class="tag">Trunk</span>

                    <span class="tag">STP</span>

                    <span class="tag">EtherChannel</span>

                    <span class="tag">OSPF</span>

                    <span class="tag">EIGRP</span>

                    <span class="tag">BGP</span>

                    <span class="tag">HSRP / VRRP</span>

                    <span class="tag">NAT</span>

                    <span class="tag">DHCP</span>

                </div>

            </div>



            <!-- CYBERSECURITE -->

            <div class="card">

                <h3>
                    🛡️ Cybersécurité
                </h3>

                <div class="tags">

                    <span class="tag">
                        ACL
                    </span>

                    <span class="tag">
                        SSH
                    </span>

                    <span class="tag">
                        DHCP Snooping
                    </span>

                    <span class="tag">
                        Port Security
                    </span>

                    <span class="tag">
                        VPN / IPsec
                    </span>

                    <span class="tag">
                        Wi-Fi Security
                    </span>

                    <span class="tag">
                        Threat Detection
                    </span>

                    <span class="tag">
                        Incident Response
                    </span>

                    <span class="tag">
                        Phishing
                    </span>

                </div>

            </div>



            <!-- OUTILS -->

            <div class="card">

                <h3>
                    🧰 Outils
                </h3>

                <div class="tags">

                    <span class="tag">
                        Cisco IOS
                    </span>

                    <span class="tag">
                        Packet Tracer
                    </span>

                    <span class="tag">
                        GNS3
                    </span>

                    <span class="tag">
                        VMware
                    </span>

                    <span class="tag">
                        Wireshark
                    </span>

                    <span class="tag">
                        Linux
                    </span>

                    <span class="tag">
                        Git
                    </span>

                    <span class="tag">
                        GitHub
                    </span>

                </div>

            </div>


        </div>

    </div>

</section>



<!-- =========================
     PROJETS
========================== -->

<section id="projets">

    <div class="container">

        <div class="section-header">

            <div class="section-label">
                Portfolio
            </div>

            <h2>
                Mes projets
            </h2>

            <p>
                Des projets conçus pour transformer
                la théorie en compétences pratiques.
            </p>

        </div>


        <div class="projects-grid">


            <!-- PROJET 1 -->

            <article class="card project">

                <div class="project-number">
                    01 — RÉSEAUX & SÉCURITÉ
                </div>

                <h3>
                    Réseau d'entreprise sécurisé
                </h3>

                <p>

                    Conception d'une infrastructure Cisco
                    avec segmentation réseau, routage,
                    ACL, NAT, SSH, DHCP Snooping,
                    VPN et supervision.

                </p>

                <div class="tags">

                    <span class="tag">
                        Cisco
                    </span>

                    <span class="tag">
                        VLAN
                    </span>

                    <span class="tag">
                        ACL
                    </span>

                    <span class="tag">
                        VPN
                    </span>

                </div>

                <a
                    class="project-link"
                    href="https://github.com/TON-USERNAME/reseau-entreprise-securise"
                    target="_blank">

                    Voir sur GitHub →

                </a>

            </article>



            <!-- PROJET 2 -->

            <article class="card project">

                <div class="project-number">
                    02 — IoT & SÉCURITÉ URBAINE
                </div>

                <h3>
                    Surveillance intelligente & IoT
                </h3>

                <p>

                    Architecture de surveillance combinant
                    caméras IP, PoE, NVR, routeurs,
                    firewall, VPN et segmentation réseau.

                </p>

                <div class="tags">

                    <span class="tag">
                        IoT
                    </span>

                    <span class="tag">
                        Cisco
                    </span>

                    <span class="tag">
                        VPN
                    </span>

                    <span class="tag">
                        Wireshark
                    </span>

                </div>

                <a
                    class="project-link"
                    href="https://github.com/TON-USERNAME/surveillance-iot-reseau"
                    target="_blank">

                    Voir sur GitHub →

                </a>

            </article>



            <!-- PROJET 3 -->

            <article class="card project">

                <div class="project-number">
                    03 — RECHERCHE CYBERSÉCURITÉ
                </div>

                <h3>
                    Détection des arnaques en ligne
                </h3>

                <p>

                    Conception d'une solution intelligente
                    visant à aider les utilisateurs à identifier
                    rapidement les signes d'une tentative
                    d'arnaque en ligne.

                </p>

                <div class="tags">

                    <span class="tag">
                        Cybersécurité
                    </span>

                    <span class="tag">
                        IA
                    </span>

                    <span class="tag">
                        Détection
                    </span>

                    <span class="tag">
                        Recherche
                    </span>

                </div>

                <a
                    class="project-link"
                    href="https://github.com/TON-USERNAME/detection-arnaques-en-ligne"
                    target="_blank">

                    Voir sur GitHub →

                </a>

            </article>



            <!-- PROJET 4 -->

            <article class="card project">

                <div class="project-number">
                    04 — CISCO LABS
                </div>

                <h3>
                    Routing & Haute disponibilité
                </h3>

                <p>

                    Laboratoires pratiques autour du routage
                    statique, des routes flottantes,
                    OSPF, EIGRP, BGP, HSRP et VRRP.

                </p>

                <div class="tags">

                    <span class="tag">
                        Routing
                    </span>

                    <span class="tag">
                        OSPF
                    </span>

                    <span class="tag">
                        EIGRP
                    </span>

                    <span class="tag">
                        BGP
                    </span>

                </div>

                <a
                    class="project-link"
                    href="https://github.com/TON-USERNAME/cisco-routing-labs"
                    target="_blank">

                    Voir sur GitHub →

                </a>

            </article>


        </div>

    </div>

</section>



<!-- =========================
     PARCOURS
========================== -->

<section id="parcours">

    <div class="container">

        <div class="section-header">

            <div class="section-label">
                Roadmap
            </div>

            <h2>
                Ma feuille de route
            </h2>

            <p>
                Une progression centrée sur la maîtrise
                des infrastructures et la sécurité opérationnelle.
            </p>

        </div>


        <div class="roadmap">


            <div class="roadmap-item">

                <div class="roadmap-number">
                    01
                </div>

                <h3>
                    Réseaux
                </h3>

                <p>
                    Routing, switching
                    et architecture réseau.
                </p>

            </div>


            <div class="roadmap-item">

                <div class="roadmap-number">
                    02
                </div>

                <h3>
                    Sécurité réseau
                </h3>

                <p>
                    Segmentation, filtrage,
                    VPN et durcissement.
                </p>

            </div>


            <div class="roadmap-item">

                <div class="roadmap-number">
                    03
                </div>

                <h3>
                    Détection
                </h3>

                <p>
                    Wireshark, logs,
                    SIEM et analyse des menaces.
                </p>

            </div>


            <div class="roadmap-item">

                <div class="roadmap-number">
                    04
                </div>

                <h3>
                    SOC
                </h3>

                <p>
                    Supervision, investigation
                    et réponse aux incidents.
                </p>

            </div>


        </div>

    </div>

</section>



<!-- =========================
     CONTACT
========================== -->

<section id="contact">

    <div class="container">

        <div class="contact-box">

            <div class="section-label">
                Contact
            </div>

            <h2>
                Construisons quelque chose de sécurisé.
            </h2>

            <p>

                Je suis ouvert aux projets réseaux,
                cybersécurité, IoT, laboratoires techniques
                et collaborations.

            </p>


            <div class="buttons">


                <!-- GITHUB -->

                <a
                    class="btn"
                    href="https://github.com/TON-USERNAME"
                    target="_blank">

                    GitHub

                </a>


                <!-- EMAIL -->

                <a
                    class="btn"
                    href="mailto:TON-EMAIL">

                    Email

                </a>


                <!-- LINKEDIN -->

                <a
                    class="btn"
                    href="https://www.linkedin.com/in/TON-LINKEDIN"
                    target="_blank">

                    LinkedIn

                </a>


            </div>

        </div>

    </div>

</section>



<!-- =========================
     FOOTER
========================== -->

<footer>

    © 2026 Joel Guei

    <br>

    Réseaux • Cybersécurité • IoT • Innovation

</footer>


</body>
</html>
