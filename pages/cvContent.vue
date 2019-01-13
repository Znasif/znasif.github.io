<template>
    <div>
        <div v-if="isPaper" class="cv-header">
            <img class="logo" src="/imgs/logos/logo-black.svg">
            <div class="name">
                <h1>Nasif Zaman</h1>
                <p class="subtitle">Graduate &bull; 3D Computer Vision Research</p>
            </div>
            <div class="links">
                <icon-link to="https://znasif.github.io" icon="web" size="">znasif.github.io</icon-link>
                <icon-link
                    to="mailto:nasifzaman@yahoo.com"
                    icon="email"
                    size=""
                >nasifzaman@yahoo.com</icon-link>
                <icon-link
                    to="https://github.com/Znasif"
                    icon="github-circle"
                    size=""
                >github.com/Znasif</icon-link>
            </div>
        </div>
        <div slot="content">
            <h2>Education</h2>
            <cv-entry
                location="Dhaka, Bangladesh"
                dates="2018"
                title="Bangladesh University of Engineering and Technology"
                subtitle="BSc Computer Science<br>
                    GPA: 3.31 / 4.0<br>
                    Honors Thesis: <i>Mouza Map Digitization</i>"
            ></cv-entry>
            <h2>Research</h2>
            <cv-entry
                location="Dhaka, Bangladesh"
                title="Computer Vision Research"
                subtitle="Prof. Monirul Islam"
                :tasks="[
                    {date: '2019 --',
                     task: 'Maple: Robust Map Segmentation Using Mask-RCNN'}]"
            ></cv-entry>
            <h2>Scholarships</h2>
            <cv-award date="2011" award="Board Scholarship in Secondary School Certificate Examination"></cv-award>
            <cv-award date="2011" award="Board Talentpool Scholarship in Primary School"></cv-award>
            <!-- <h2>Awards</h2>
            <cv-award date="2018" award="Research Assistant, Bangladesh University of Engineering and Technology"></cv-award>
            <h2 v-if="isPaper">Papers</h2>
            <publication-list
                v-if="isPaper"
                highlight-author="Nasif"
                :type-filter="['inproceedings', 'article']"
                :showLinks="false"
            ></publication-list>
            <h2 v-if="isPaper">Conference Abstracts and Posters</h2>
            <publication-list
                v-if="isPaper"
                highlight-author="Ebert"
                :type-filter="['poster']"
                :showLinks="false"
            ></publication-list>
            <h2 v-if="!isPaper">Publications</h2>
            <p v-if="!isPaper">See
                <nuxt-link to="/publications">publications section</nuxt-link>
            </p>
            <h2>Talks</h2>
            <publication-list
                highlight-author="Ebert"
                :type-filter="['talk']"
                :showLinks="false">
            </publication-list>
            - UQ lecture
            - CS 189 guest lecture
            - AAMAS 2018?
            - Wyss molecular robotics
            <h2>Teaching</h2>
            <cv-entry
                location="Cambridge, MA"
                title="Harvard University"
                :tasks="[
                    {date: 'Fall 2018',
                     task: '<b>Teaching Staff,</b> How To Make (Almost) Anything, Harvard section'},
                    {date: 'Spring 2018',
                     task: '<b>Teaching Fellow,</b> CS 189: Autonomous Robot Systems'}]"
            ></cv-entry>
            <cv-entry
                location="Boston, MA"
                title="Northeastern University"
                :tasks="[
                    {date: '2014 -- 2015',
                     task: '<b>Teaching Assistant,</b> CS 2510: Fundamentals of Computer Science (2 semesters)'},
                    {date: '2012 -- 2014',
                     task: '<b>Tutor,</b> CS 2510: Fundamentals of Computer Science (3 semesters)'},
                    {date: '2011 -- 2013',
                     task: '<b>Undergraduate Mentor,</b> Proactive Recruitment in Science and Mathematics (PRISM)'}]"
            ></cv-entry>
            <h2>Outreach and Service</h2>
            <cv-award date="2018" award="Robot Design Judge, FIRST LEGO League Newton Qualifier"></cv-award>
            <cv-award
                date="2018"
                award="Speaker, Science in the News fall lecture series: &quot;Brains and Bodies: How to Make Smart Robots&quot;"
            ></cv-award>
            <cv-award date="2018" award="Guest, <i>Brains On!</i> science podcast live show"></cv-award>
            <cv-award date="2017, 2018" award="Volunteer, Boston Public Schools Science Fair"></cv-award>
            <cv-award date="2016" award="Volunteer, EuroHaptics 2016"></cv-award>
            <cv-award date="2010 -- 2015" award="Volunteer, Northeastern Civic Engagement Program"></cv-award>
            <cv-award date="2014" award="Tutor team leader, TechBoston Academy"></cv-award>
            <cv-award
                date="2014"
                award="Teacher, NEU Splash Program. Class: &quot;This is your Brain&quot;"
            ></cv-award>
            <cv-award date="2011 -- 2013" award="Volunteer, Brigham and Women's Hospital"></cv-award>
            <cv-award
                date="2010 -- 2011"
                award="Mentor, Massachusetts General Hospital Youth Program"
            ></cv-award>
            -->
            <h2>Work Experience</h2>
            <cv-entry
                location="Dhaka, Bangladesh"
                title="Elab"
                subtitle="Machine Learning and Big Data Engineer"
                :tasks="[
                    {date: '2018 -- 2018',
                     task: 'Processing and Analyzing Imaging Data'},
                    {date: '2018 -- 2018',
                     task: 'Extract Text from Medical Reports'},
                    {date: '2018 -- 2018',
                     task: 'Train Neural Network for Tentative Diagnosis'},
                    {date: '2018 -- 2018',
                     task: 'Migrate Infrastructure to Google Cloud Platform'},
                    {date: '2019 --',
                     task: 'Create a functional REST API'}]"
            ></cv-entry>
            <h2>Skills</h2>
            <cv-skill
                category="Programming"
                :skills="[
                'Python (including Django, NumPy)', 'Java (including Spring)', 'MATLAB', 'C/C++ (including AVR, Arduino)',
                'C#', 'HTML/CSS', 'LaTeX']"
            ></cv-skill>
            <cv-skill
                category="Computer Vision and Image Processing"
                :skills="[
                'OpenCV', 'Matplotlib', 'Caffe', 'Keras', 'PyTorch',
                'scikit-learn', 'Unity3D', 'Blender', 'VisualSFM',
                'Google Cloud Platform']"
            ></cv-skill>
            <cv-skill
                category="GIS and Cartography"
                :skills="[
                'ArcScene', 'ArcGIS']"
            ></cv-skill>
            <h2>Relevant Coursework</h2>
            <cv-skill
                category="Computer Science"
                :skills="[
                'Artificial Intelligence', 'Computational Geometry', 'Linear Algebra',
                'Digital Image Processing', 'Computer Graphics']"
            ></cv-skill>
            <cv-skill
                category="Online Coursework"
                :skills="[
                'Neural Networks and Deep Learning', 'Probabilistic Graphical Models', 
                'Multi-view Geometry', 'Machine Vision', 'Introduction to XR',
                'Game Theory', 'Fundamentals of GIS']"
            ></cv-skill>
            <h2>Projects</h2>
            <cv-award date="2018" award="Bangla Numeral Detection and Recognition in Scanned Mouza Maps with MaskRCNN and OCR (Python)"></cv-award>
            <cv-award date="2018" award="Reddit bot for Map Recognition in r/Map_Porn, r/MapPorn and r/maps (Python)"></cv-award>
            <cv-award date="2017" award="Plot Information Management System (Django)"></cv-award>
            <cv-award date="2016" award="Train Ticket Reservation System (Java and Oracle)"></cv-award>
            <cv-award date="2015" award="Multi Tab Web Browser (Java)"></cv-award>
            <cv-award date="2014" award="2D Racing Car (C)"></cv-award>
            <h2>Hardware Projects</h2>
            <cv-award date="2018" award="Grid Solving Robot (Arduino Uno and IR-Sensor)']"></cv-award>
            <cv-award date="2017" award="2-Player Ludo Game (Variants: Player1 vs Robot and Player1 vs Player2) (ATmega32 and LED Matrix)"></cv-award>
            <h2>Activities and Interests</h2>
            <cv-skill
                category="Sport"
                :skills="[
                'Swimming', 'Cycling']"
            ></cv-skill>
            <cv-skill
                category="Other"
                :skills="[
                'Map making', 'Web crawling', 'Casual reading', 'Eating']"
            ></cv-skill>
        </div>
    </div>
</template>

<script>
import PublicationList from "~/components/PublicationList.vue";
import CvEntry from "~/components/cv/CvEntry.vue";
import CvAward from "~/components/cv/CvAward.vue";
import CvSkill from "~/components/cv/CvSkill.vue";
import IconLink from "~/components/IconLink.vue";

export default {
  components: {
    PublicationList,
    CvEntry,
    CvAward,
    CvSkill,
    IconLink
  },
  props: {
    isPaper: { default: false }
  }
};
</script>