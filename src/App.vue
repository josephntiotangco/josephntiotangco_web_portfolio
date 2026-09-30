<script setup>
import { computed, ref } from "vue";

const profile = {
  name: "Joseph Nunag-Tiotangco",
  role: "Software Engineer",
  summary:
    "Software Engineer experienced in business application development, system enhancement, API and database-backed workflows, production support, and full-stack project implementation. My background in audit and business analysis gives me a stronger ability to understand business rules, trace issues, and build practical software solutions.",
  links: [
    {
      label: "GitHub",
      href: "https://github.com/josephntiotangco"
    },
    {
      label: "ATOP Demo",
      href: "https://auditortimeoutputprogress.vercel.app/"
    },
    {
      label: "KFPT Demo",
      href: "https://kfpt-web.vercel.app/"
    }
  ]
};

const capabilities = [
  {
    title: "Application Engineering",
    details:
      "C#, .NET, Ruby on Rails, PHP, Avalonia UI, WPF, Xamarin Forms, issue analysis, debugging, maintenance, and production support."
  },
  {
    title: "Business Systems",
    details:
      "Requirements analysis, functional specifications, workflow review, user acceptance testing, go-live support, and client issue handling."
  },
  {
    title: "Full-Stack Development",
    details:
      "Vue, Vite, Pinia, Axios, ASP.NET Core Web API, authentication flows, dashboards, reports, and database-backed applications."
  },
  {
    title: "Mobile and Utilities",
    details:
      ".NET MAUI, Kotlin Android, Jetpack Compose, Room, WorkManager, QR scanning, SMS scheduling, and local data workflows."
  }
];

const workExperience = [
  {
    company: "Iripple Inc.",
    period: "March 2019 - Present",
    roles: [
      "Business Analyst",
      "Senior Business Analyst",
      "Senior Software Developer",
      "Software Engineer"
    ],
    summary:
      "Current Software Engineer role after progressing from business analysis into software development. Work includes POS systems, ERP integration, API support, client enhancements, production issue fixing, deployment support, user acceptance testing, and business-rule implementation."
  },
  {
    company: "Eastern Telecommunications Philippines Inc.",
    period: "March 2018 - March 2019",
    roles: ["Auditor III"],
    summary:
      "Handled operations audit, process review, audit planning, SAP MM utilization review, customer activation review, billing systems, and inventory systems post-implementation review."
  },
  {
    company: "Puregold Price Club Inc.",
    period: "August 2013 - March 2018",
    roles: ["Audit Assistant", "Junior Auditor", "Internal Audit roles"],
    summary:
      "Built foundation in information systems audit, data integrity review, access control review, SDLC quality assurance, process automation, audit supervision, and documentation."
  }
];

const projects = [
  {
    name: "ATOP - Auditor Time Output Progress",
    type: "Full-stack audit workflow",
    stack: ["ASP.NET Core Web API", "Vue 3", "Entity Framework Core", "MySQL", "JWT"],
    summary:
      "Audit workflow system for workspace registration, task management, auditor daily updates, dashboard monitoring, report submission, and reviewer workflow.",
    link: "https://auditortimeoutputprogress.vercel.app/"
  },
  {
    // name: "EcomAPI_kfpt and VueKFPTWeb_Mod",
    //JT-2026/08/13 - simplify deployed project display name
    name: "KFPT Web",
    type: "E-commerce web system",
    stack: ["ASP.NET Core", "Vue", "Pinia", "Axios", "SQL Server"],
    summary:
      "Backend API and frontend web application covering products, categories, cart, orders, authentication, password reset, email confirmation, and order management.",
    link: "https://kfpt-web.vercel.app/"
  },
  {
    name: "FriendLy Ice Breaker",
    type: "Cross-platform mobile app",
    stack: [".NET MAUI", "C#", "XAML", "Local JSON"],
    summary:
      "Bilingual mobile app with English and Filipino randomized conversation prompts, local question banks, language selection, and mobile-first UI flow."
  },
  {
    name: "SMS Scheduler",
    type: "Android utility",
    stack: ["Kotlin", "Jetpack Compose", "Room", "WorkManager", "SmsManager"],
    summary:
      "Android application for composing, sending, and scheduling SMS messages with recipient groups, contacts integration, selected weekday schedules, and reboot handling."
  },
  {
    name: "QRCodeScanner",
    type: "Mobile scanner",
    stack: [".NET MAUI", "ZXing.Net.Maui", "Camera API"],
    summary:
      "QR scanning utility that detects QR values through the camera, displays scanned results, opens valid links, and supports reset behavior."
  }
];

const trainings = [
  //JT-2026/09/30 - add ai champion recognition credential
  {
    title: "AI Champion",
    meta: "iRipple Inc. - Certificate of Recognition",
    focus:
      "Recognized for AI fluency, innovative use of artificial intelligence, and applying AI to improve productivity and create meaningful organizational impact."
  },
  {
    title: "Foundational C# with Microsoft",
    meta: "freeCodeCamp / Microsoft - 2025",
    focus: "C# fundamentals and .NET development foundation"
  },
  {
    title: "Vue 3 and .NET Full-Stack Real World App",
    meta: "Udemy - 2025",
    focus: "Vue frontend, .NET backend, and full-stack application workflow"
  },
  {
    title: "MS Tech Sessions - Xamarin Hands-On Session",
    meta: "Mobile .NET Developers Philippines - 2020",
    focus: "Mobile development exposure within the .NET ecosystem"
  },
  {
    title: "Business Analysis",
    meta: "Mapua University - 2018",
    focus: "Requirements analysis, documentation, and process understanding"
  },
  {
    title: "IT Project Management",
    meta: "BusinessCoach Inc. - 2018",
    focus: "Project coordination, planning, and implementation support"
  },
  {
    title: "Innovative Thinking System Workshop",
    meta: "ACG Human Capital Solutions Corporation - 2018",
    focus: "Structured problem solving, creative thinking, and process improvement"
  },
  {
    title: "Networking with Windows Active Server",
    meta: "CNCTC - 2015",
    focus: "Networking and server administration foundation"
  },
  {
    title: "PC Troubleshooting and Networking",
    meta: "Microcadd - 2015",
    focus: "Computer hardware, troubleshooting, and networking fundamentals"
  }
];

const education = [
  {
    degree: "Master in Information Technology - 30 academic units completed",
    school: "Pamantasan ng Lungsod ng Maynila",
    focus:
      "Graduate-level IT coursework that strengthened my foundation in systems analysis, software development concepts, database-oriented thinking, IT project work, research discipline, and the broader role of information systems in organizations."
  },
  {
    degree: "Bachelor of Science in Commerce, Major in Internal Auditing",
    school: "Far Eastern University",
    focus:
      "Developed the analytical, documentation, control review, risk assessment, and evidence-based thinking that later supported my work in information systems audit, business analysis, and software engineering."
  }
];

const evidenceItems = [
  {
    image: "/assets/fb-nov-2021.jpg",
    caption: "Early desktop application post"
  },
  {
    image: "/assets/fb-aug-2025.jpg",
    caption: "QR and free website project post"
  },
  {
    image: "/assets/fb-jul-2025.jpg",
    caption: "KFPT web application public post"
  },
  {
    image: "/assets/fb-oct-2025.jpg",
    caption: "Desktop application memory post"
  },
  {
    image: "/assets/fb-apr-2026.jpg",
    caption: "FriendLy Ice Breaker mobile app post"
  }
];

//JT-2026/08/11 - add public writing evidence to support the career transition timeline
const writingItems = [
  {
    title: "From Internal Auditor to Software Engineer",
    platform: "DEV Community - August 2020",
    summary:
      "A public career-transition article written during the pandemic period, documenting my move from audit and process work into software development.",
    link: "https://dev.to/josephntiotangco/from-internal-auditor-to-software-engineer-21gf"
  }
];

const selectedEvidence = ref(0);

const currentEvidence = computed(() => evidenceItems[selectedEvidence.value]);

function moveEvidence(direction) {
  selectedEvidence.value =
    (selectedEvidence.value + direction + evidenceItems.length) % evidenceItems.length;
}
</script>

<template>
  <header class="topbar">
    <a class="brand" href="#top" aria-label="Joseph Nunag-Tiotangco portfolio">
      <!-- <span class="brandMark">JT</span> -->
      <!-- JT-2026/08/13 - use personal logo as the portfolio brand mark -->
      <img class="brandMark" src="/assets/jt-logo-192.png" alt="" aria-hidden="true" />
      <span>{{ profile.name }}</span>
    </a>
    <nav class="nav" aria-label="Primary navigation">
      <a href="#experience">Experience</a>
      <a href="#projects">Projects</a>
      <a href="#writing">Writing</a>
      <a href="#evidence">Evidence</a>
      <a href="#training">Training</a>
      <a href="#education">Education</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <main id="top">
    <section class="hero" aria-labelledby="hero-title">
      <div class="heroCopy">
        <p class="eyebrow">{{ profile.role }}</p>
        <h1 id="hero-title">Software Engineer building practical business applications and full-stack systems.</h1>
        <p class="heroText">{{ profile.summary }}</p>
        <div class="roleStrip" aria-label="Software engineering focus areas">
          <span>Current Software Engineer</span>
          <span>.NET and Vue</span>
          <span>API and database workflows</span>
          <span>Production support</span>
        </div>
        <div class="heroActions" aria-label="Profile links">
          <a
            v-for="link in profile.links"
            :key="link.href"
            class="button"
            :class="{ primary: link.label === 'GitHub' }"
            :href="link.href"
            target="_blank"
            rel="noreferrer"
          >
            {{ link.label }}
          </a>
        </div>
      </div>

      <aside class="profileCard" aria-label="Profile summary">
        <img src="/assets/profile.jpg" :alt="`Portrait of ${profile.name}`" />
        <div>
          <h2>{{ profile.name }}</h2>
          <p>
            Software Engineer working on .NET, Vue, APIs, system enhancements, and production support.
          </p>
        </div>
      </aside>
    </section>

    <section class="section" aria-labelledby="capability-title">
      <div class="sectionHeading">
        <p class="eyebrow">Capability</p>
        <h2 id="capability-title">Technical capability grounded in workplace execution.</h2>
      </div>
      <div class="capabilityGrid">
        <article v-for="capability in capabilities" :key="capability.title">
          <h3>{{ capability.title }}</h3>
          <p>{{ capability.details }}</p>
        </article>
      </div>
    </section>

    <section id="experience" class="section muted" aria-labelledby="experience-title">
      <div class="sectionHeading">
        <p class="eyebrow">Work Experience</p>
        <h2 id="experience-title">Software engineering role strengthened by audit and business analysis experience.</h2>
      </div>
      <div class="timeline">
        <article v-for="job in workExperience" :key="job.company" class="timelineItem">
          <div>
            <p class="period">{{ job.period }}</p>
            <h3>{{ job.company }}</h3>
            <p class="roles">{{ job.roles.join(" / ") }}</p>
          </div>
          <p>{{ job.summary }}</p>
        </article>
      </div>
    </section>

    <section id="projects" class="section" aria-labelledby="projects-title">
      <div class="sectionHeading">
        <p class="eyebrow">Selected Projects</p>
        <h2 id="projects-title">Side projects and deployed applications.</h2>
      </div>
      <div class="projects">
        <article v-for="project in projects" :key="project.name" class="project">
          <p class="projectType">{{ project.type }}</p>
          <h3>{{ project.name }}</h3>
          <p>{{ project.summary }}</p>
          <ul>
            <li v-for="item in project.stack" :key="item">{{ item }}</li>
          </ul>
          <a v-if="project.link" :href="project.link" target="_blank" rel="noreferrer">
            View deployed app
          </a>
        </article>
      </div>
    </section>

    <section id="writing" class="section" aria-labelledby="writing-title">
      <div class="sectionHeading">
        <p class="eyebrow">Writing</p>
        <h2 id="writing-title">Public writing that supports my software engineering journey.</h2>
      </div>
      <div class="writingGrid">
        <article v-for="item in writingItems" :key="item.title" class="writingItem">
          <p class="writingMeta">{{ item.platform }}</p>
          <h3>{{ item.title }}</h3>
          <p>{{ item.summary }}</p>
          <a :href="item.link" target="_blank" rel="noreferrer">
            Read article
          </a>
        </article>
      </div>
    </section>

    <section id="evidence" class="section muted" aria-labelledby="evidence-title">
      <div class="sectionHeading">
        <p class="eyebrow">Public Evidence</p>
        <h2 id="evidence-title">Repository, deployed apps, and public project timeline.</h2>
      </div>
      <div class="evidenceLayout">
        <div class="evidenceCopy">
          <p>
            These links and selected public posts support the timeline and authenticity of project
            work. They are presented as professional portfolio evidence and public project references.
          </p>
          <dl class="linkList">
            <div>
              <dt>GitHub</dt>
              <dd>
                <a href="https://github.com/josephntiotangco" target="_blank" rel="noreferrer">
                  github.com/josephntiotangco
                </a>
              </dd>
            </div>
            <div>
              <dt>KFPT Web</dt>
              <dd>
                <a href="https://kfpt-web.vercel.app/" target="_blank" rel="noreferrer">
                  kfpt-web.vercel.app
                </a>
              </dd>
            </div>
            <div>
              <dt>ATOP</dt>
              <dd>
                <a
                  href="https://auditortimeoutputprogress.vercel.app/"
                  target="_blank"
                  rel="noreferrer"
                >
                  auditortimeoutputprogress.vercel.app
                </a>
              </dd>
            </div>
          </dl>
        </div>

        <div class="evidenceGallery" aria-label="Selected public project posts">
          <button type="button" aria-label="Previous evidence" @click="moveEvidence(-1)">‹</button>
          <figure>
            <img :src="currentEvidence.image" :alt="currentEvidence.caption" />
            <figcaption>{{ currentEvidence.caption }}</figcaption>
          </figure>
          <button type="button" aria-label="Next evidence" @click="moveEvidence(1)">›</button>
        </div>
      </div>
    </section>

    <section id="training" class="section" aria-labelledby="training-title">
      <div class="sectionHeading">
        <p class="eyebrow">Training & Certifications</p>
        <h2 id="training-title">Selected learning that supports my engineering practice.</h2>
      </div>
      <div class="trainingGrid">
        <article v-for="training in trainings" :key="training.title" class="trainingItem">
          <div>
            <h3>{{ training.title }}</h3>
            <p class="trainingMeta">{{ training.meta }}</p>
          </div>
          <p>{{ training.focus }}</p>
        </article>
      </div>
    </section>

    <section id="education" class="section muted" aria-labelledby="education-title">
      <div class="sectionHeading">
        <p class="eyebrow">Education</p>
        <h2 id="education-title">Academic background that supports my software engineering path.</h2>
      </div>
      <div class="educationGrid">
        <article v-for="item in education" :key="item.degree" class="educationItem">
          <p class="educationSchool">{{ item.school }}</p>
          <h3>{{ item.degree }}</h3>
          <p>{{ item.focus }}</p>
        </article>
      </div>
    </section>

    <section id="contact" class="section closingSection" aria-labelledby="contact-title">
      <div class="sectionHeading">
        <p class="eyebrow">Contact</p>
        <h2 id="contact-title">Software Engineer open to application development and full-stack opportunities.</h2>
      </div>
      <div class="closing">
        <p>
          This portfolio highlights my software engineering experience in business applications,
          APIs, frontend development, mobile utilities, database-backed workflows, and systems support.
        </p>
        <a class="button primary" href="https://github.com/josephntiotangco" target="_blank" rel="noreferrer">
          Review GitHub
        </a>
      </div>
    </section>
  </main>

  <footer>
    <span>{{ profile.name }}</span>
    <span>Software Engineering Portfolio</span>
  </footer>
</template>
