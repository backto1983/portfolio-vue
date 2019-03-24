<template>
<div class="main-wrapper">
  <body id="page-top">
    <nav class="navbar navbar-expand-lg navbar-dark bg-primary fixed-top" id="sideNav">
      <a class="navbar-brand js-scroll-trigger" href="#page-top">
        <span class="d-block d-lg-none">Professional Portfolio</span>
        <span class="d-none d-lg-block">
          <img
            class="img-fluid img-profile rounded-circle mx-auto mb-2"
            src="../src/assets/profile.jpg"
            alt="Profile picture"
          >
        </span>
      </a>
      <button
        class="navbar-toggler"
        type="button"
        data-toggle="collapse"
        data-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav">
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#about">About</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#experience">Experience</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#education">Education</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#skills">Skills</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#projects">Projects</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#interests">Interests</a>
          </li>
        </ul>
      </div>
    </nav>

    <div class="container-fluid p-0">
      <section class="resume-section p-3 p-lg-5 d-flex align-items-center" id="about">
        <div class="w-100">
          <h1 class="mb-0">
            {{ name }}
            <span class="text-primary">{{ surname }}</span>
          </h1>
          <div class="subheading mb-5">
            {{ address }}
            <a href="mailto:hnrq.ornellas@gmail.com">{{ email }}</a>
          </div>
          <p class="lead mb-5">{{ aboutMe }}</p>
          <div class="social-icons">
            <a href="https://www.linkedin.com/in/henrique-oliveira-501a5a116/" target="_blank">
              <i class="fab fa-linkedin"></i>
            </a>
            <a href="https://github.com/backto1983?tab=repositories" target="_blank">
              <i class="devicon-github-plain-wordmark"></i>
            </a>
            <a href="https://www.facebook.com/profile.php?id=100005166099272" target="_blank">
              <i class="devicon-facebook-plain"></i>
            </a>
          </div>
        </div>
      </section>

      <hr class="m-0">

      <section class="resume-section p-3 p-lg-5 d-flex justify-content-center" id="experience">
        <div class="my-auto">
          <h2 class="mb-5">Experience</h2>

          <div
            class="resume-item d-flex flex-column flex-md-row mb-5"
            v-for="job in experience"
            :key="job.description"
          >
            <div class="resume-content mr-auto">
              <h3 class="mb-0">{{ job.position }}</h3>
              <div class="subheading mb-3">{{ job.company }}</div>
              <p>{{ job.description }}</p>
            </div>
            <div class="resume-date text-md-right">
              <span class="text-primary">{{ job.startDate }} - {{ job.endDate }}</span>
            </div>
          </div>
        </div>
      </section>

      <hr class="m-0">

      <section class="resume-section p-3 p-lg-5 d-flex align-items-center" id="education">
        <div class="w-100">
          <h2 class="mb-5">Education</h2>

          <div class="resume-item d-flex flex-column flex-md-row justify-content-between mb-5">
            <div class="resume-content">
              <h3 class="mb-0">Georgian College</h3>
              <div class="subheading mb-3">Computer Programmer - Graduated with Honours</div>
              <p>GPA: 87</p>
            </div>
            <div class="resume-date text-md-right">
              <span class="text-primary">Jan 2017 - Dec 2018</span>
            </div>
          </div>

          <div class="resume-item d-flex flex-column flex-md-row justify-content-between mb-5">
            <div class="resume-content">
              <h3 class="mb-0">Universidade Federal de Minas Gerais</h3>
              <div class="subheading mb-3">Master's in Plant Taxonomy</div>
              <p>GPA: 85</p>
            </div>
            <div class="resume-date text-md-right">
              <span class="text-primary">Mar 2008 - Mar 2010</span>
            </div>
          </div>

          <div class="resume-item d-flex flex-column flex-md-row justify-content-between">
            <div class="resume-content">
              <h3 class="mb-0">Pontifícia Universidade Católica de Minas Gerais</h3>
              <div class="subheading mb-3">Bachelor's in Biology</div>
              <p>GPA: 84</p>
            </div>
            <div class="resume-date text-md-right">
              <span class="text-primary">Aug 2002 - Jun 2008</span>
            </div>
          </div>
        </div>
      </section>

      <hr class="m-0">

      <section class="resume-section p-3 p-lg-5 d-flex align-items-center" id="skills">
        <div class="w-100">
          <h2 class="mb-5">Skills</h2>
          <p class="subheading mb-3">Programming Languages &amp; Tools</p>
          <ul class="list-inline dev-icons">
            <li class="list-inline-item">
              <i class="devicon-java-plain-wordmark"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicon-mysql-plain-wordmark"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicon-mongodb-plain-wordmark"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicon-html5-plain-wordmark"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicon-css3-plain-wordmark"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicon-javascript-plain"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicon-nodejs-plain-wordmark"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicon-wordpress-plain-wordmark"></i>
            </li>
          </ul>
        </div>
      </section>

      <hr class="m-0">

      <section class="resume-section p-3 p-lg-5 d-flex align-items-center" id="projects">
        <div class="w-100">
          <h2 class="mb-5">Projects</h2>
          <p>Click the images below to follow the links</p>

          <div class="container">
            <div class="row">
              <div class="col-sm" style="padding: 20px">
                <a href="http://www.johnboddyhomes.ca" target="_blank">
                  <img
                    src="../src/assets/jbh_thumbnail.png"
                    alt="John Boddy Homes Website"
                    class="img-thumbnail"
                  >
                </a>
                <figcaption class="figure-caption">John Boddy Homes Website</figcaption>
              </div>

              <!-- http://s000.tinyupload.com/?del_id=07660950018026954757 -> to delete file -->
              <div class="col-sm" style="padding: 20px">
                <a href="http://s000.tinyupload.com/?file_id=00009100766679264300" target="_blank">
                  <img src="../src/assets/java.png" alt="Java Application" class="img-thumbnail">
                </a>
                <figcaption class="figure-caption">Java Application</figcaption>
              </div>
            </div>
          </div>
        </div>
      </section>

      <hr class="m-0">

      <section class="resume-section p-3 p-lg-5 d-flex align-items-center" id="interests">
        <div class="w-100">
          <h2 class="mb-5">Interests</h2>
          <p>Besides my interests in computer programming and biology, I enjoy physical activities, especially outdoors. Football, running, hiking and swimming are my favorite sports.</p>
          <p
            class="mb-0"
          >Also, I am a fan of books, movies and tv series. Sci-Fi, Fantasy, Investigation and History are the genres that interests me the most.</p>
        </div>
      </section>
    </div>
  </body>
</div>
</template>

<script>
export default {
  data() {
    return {
      title: "My Portfolio",
      name: "HENRIQUE",
      surname: "OLIVEIRA",
      address: "(705) 790-0196 ·",
      email: "hnrq.ornellas@gmail.com",
      aboutMe:
        "I am a Computer Programmer graduate from Georgian College. My program focused on developing scripting and query languages skills, including Java, JavaScript and SQL. In the last 2 years, I have learned how to design and manipulate applications and databases.",
      experience: [
        {
          position: "Technology Analyst (CO-OP)",
          company: "Bank of Montreal",
          description:
            "Planned and conducted software analysis for inclusion in project solutions;participated in reviews and inspections to ensure the quality of work products; prepared reports and/or graphs for tracking, trending and other reporting requirements; supported the execution of improvement initiatives using data-driven insights to deliver positive outcomes.",
          startDate: "Aug 2018",
          endDate: "Dec 2018"
        },
        {
          position: "Survey Programmer (CO-OP)",
          company: "The Logit Group",
          description:
            "Used control statements to manage survey flow; assured programming quality through extensive testing; edited survey layouts using HTML and CSS; provided feedback to managers regarding project status.",
          startDate: "Aug 2017",
          endDate: "Dec 2017"
        },
        {
          position: "Custodian",
          company: "The Town of Ajax",
          description:
            "Performed cleaning and related activities to keep exterior/interior of buildings organized; assisted with setup of facilities for meetings, conferences and events; locked/unlocked assigned buildings; secured facilities when not in use following predetermined routine.",
          startDate: "Mar 2018",
          endDate: "Present"
        }
      ]
    };
  },
  mounted() {
    const $ = this.jquery;
    this.$nextTick(() => {
      $('a.js-scroll-trigger[href*="#"]:not([href="#"])').click(function() {
        if (
          location.pathname.replace(/^\//, "") ===
            this.pathname.replace(/^\//, "") &&
          location.hostname === this.hostname
        ) {
          var target = $(this.hash);
          target = target.length
            ? target
            : $("[name=" + this.hash.slice(1) + "]");
          if (target.length) {
            $("html, body").animate(
              {
                scrollTop: target.offset().top
              },
              1000,
              "easeInOutExpo"
            );
            return false;
          }
        }
      });
      //Closes responsive menu when a scroll trigger link is clicked
      $(".js-scroll-trigger").click(function() {
        $(".navbar-collapse").collapse("hide");
      });
      //Activate scrollspy to add active class to navbar items on scroll
      $("body").scrollspy({
        target: "#sideNav"
      });
    });
  }
};
</script>

<style>
body {
  font-family: "Muli", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
    "Helvetica Neue", Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji",
    "Segoe UI Symbol", "Noto Color Emoji";

  color: #868e96;
}

@media (min-width: 992px) {
  body {
    padding-top: 0;
    padding-left: 17rem;
  }
}

h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: "Saira Extra Condensed", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif, "Apple Color Emoji",
    "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji";
  font-weight: 700;
  text-transform: uppercase;
  color: #343a40;
}

h1 {
  font-size: 6rem;
  line-height: 5.5rem;
}

h2 {
  font-size: 3.5rem;
}

h3 {
  font-size: 2rem;
}

p.lead {
  font-size: 1.15rem;
  font-weight: 400;
}

.subheading {
  text-transform: uppercase;
  font-weight: 500;
  font-family: "Saira Extra Condensed", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif, "Apple Color Emoji",
    "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji";
  font-size: 1.5rem;
}

.social-icons a {
  display: inline-block;
  height: 3.5rem;
  width: 3.5rem;
  background-color: #495057;
  color: #fff !important;
  border-radius: 100%;
  text-align: center;
  font-size: 1.5rem;
  line-height: 3.5rem;
  margin-right: 1rem;
}

.social-icons a:last-child {
  margin-right: 0;
}

.social-icons a:hover {
  background-color: #11123e;
}

.dev-icons {
  font-size: 3rem;
}

.dev-icons .list-inline-item i:hover {
  color: #11123e;
}

#sideNav .navbar-nav .nav-item .nav-link {
  font-weight: 800;
  letter-spacing: 0.05rem;
  text-transform: uppercase;
}

#sideNav .navbar-toggler:focus {
  outline-color: #101011;
}

@media (min-width: 992px) {
  #sideNav {
    text-align: center;
    position: fixed;
    top: 0;
    left: 0;
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    -ms-flex-direction: column;
    flex-direction: column;
    width: 17rem;
    height: 100vh;
  }
  #sideNav .navbar-brand {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    margin: auto auto 0;
    padding: 0.5rem;
  }
  #sideNav .navbar-brand .img-profile {
    max-width: 10rem;
    max-height: 10rem;
    border: 0.5rem solid rgba(255, 255, 255, 0.2);
  }
  #sideNav .navbar-collapse {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: start;
    -ms-flex-align: start;
    align-items: flex-start;
    -webkit-box-flex: 0;
    -ms-flex-positive: 0;
    flex-grow: 0;
    width: 100%;
    margin-bottom: auto;
  }
  #sideNav .navbar-collapse .navbar-nav {
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    -ms-flex-direction: column;
    flex-direction: column;
    width: 100%;
  }
  #sideNav .navbar-collapse .navbar-nav .nav-item {
    display: block;
  }
  #sideNav .navbar-collapse .navbar-nav .nav-item .nav-link {
    display: block;
  }
}

section.resume-section {
  padding-top: 5rem !important;
  padding-bottom: 5rem !important;
  max-width: 75rem;
}

section.resume-section .resume-item .resume-date {
  min-width: none;
}

@media (min-width: 768px) {
  section.resume-section {
    min-height: 100vh;
  }
  section.resume-section .resume-item .resume-date {
    min-width: 18rem;
  }
}

@media (min-width: 992px) {
  section.resume-section {
    padding-top: 3rem !important;
    padding-bottom: 3rem !important;
  }
}

.bg-primary {
  background-color: #11123e !important;
}

.text-primary {
  color: #11123e !important;
}

a {
  color: #11123e;
}

a:hover,
a:focus,
a:active {
  color: #101011;
}
</style>