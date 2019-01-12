<template>
  <div>
    <primary-section
      title="About Me"
      subtitle="Nasif Zaman, 3d vision enthusiast"
      texture="graph-paper"
    >
      <div slot="links">
        <p class="buttons">
          <icon-button-link
            to="https://github.com/Znasif"
            icon="github-circle"
            title="GitHub"
          >GitHub</icon-button-link>
          <icon-button-link
            to="https://www.linkedin.com/in/nasifzaman-9683309a/"
            icon="linkedin"
            title="LinkedIn"
          >LinkedIn</icon-button-link>
        </p>
      </div>
      <gallery
        :img-srcs="[
      'march-for-science.jpg',
      'curling.jpg',
      ['project_night_four_web.jpg', 'Diaries']
      ]"
      ></gallery>
      <div class="block-content content">
        <vue-markdown>
I am a fresh graduate in computer science from Bangladesh University of Engineering and Technology. I am currently working as a Research Assistant developing robust segmentation algorithms to extract spatial features from a scanned map with Professor Monirul Islam. I am also a part-time machine learning engineer at [Elab](https://elab.ai). My job is to extract, process medical data and host state-of-the-art machine learning models in the google cloud platform for batch training and easy inference.

I am interested in 3D vision, multi-view geometry, cartography, and multi-modal learning. I am specifically interested in streamlining 3D content creation process to make XR interactive-learning as ubiquitous as videos. I am actively looking for graduate schools that would fit my research goals. My goal is to pursue a career in computer vision research in NVIDIA.

In my last year of undergrad, I developed an algorithm for bangla text extraction and recognition from scanned plot ownership documents and store them in a central database using Django. As my undergrad thesis, I developed an image processing algorithm that detects plot contours from a scanned mouza map. This has exposed me to the elements that I now want to do graduate research in, such as computer vision and multi-modal learning.

I also deeply care about science communication and outreach. I believe modern MOOCs are a great step towards bringing education within everyones reach. Videos are the primary medium for these courses. However, They lack interactive features. For most students (besides those that do all their work in computers), the interactive lab environment is currently missing. AR and VR research is trying to bridge that gap. But this won't be possible if 3D content creation remains inaccessible to lay users. I believe research in the field of 3D reconstruction will enable civil or mechanical engineering students to practice lab work, medical students to perform simulated surgery. The possibilities are endless.
        </vue-markdown>
        <p>In my free time, I surf
          <a href="http://reddit.com/r/MapPorn"> r/MapPorn</a>,
          <a href="http://reddit.com/r/mapmaking"> r/mapmaking</a>,
          <a href="http://reddit.com/r/MapPorn"> r/Maps</a>,
          <a href="http://reddit.com/r/MapPorn"> r/Map_Porn</a> and other such subreddits and read
          <a href="https://docs.google.com/spreadsheets/d/18Nnc6_Kncy7iILfn9m23OOTl0DAN6TQArSxB9SvUKcU/edit?usp=sharing">cool books and articles</a>
        </p>
      </div>
      <div class="block-content">
        <h1 class="title is-2 has-text-centered">See More</h1>
        <div class="has-flex-items">
          <image-block-link title="CV"></image-block-link>
          <image-block-link title="Research"></image-block-link>
          <!--<image-block-link title="Publications"></image-block-link>
          <image-block-link title="Side Projects"></image-block-link>-->
          <image-block-link title="Miscellaneous"></image-block-link>
        </div>
      </div>
      <div class="block-content">
        <h1 class="title is-2 has-text-centered">Contact Me</h1>
        <div class="buttons is-centered">
          <a class="button is-large is-primary" href="mailto:nasifzaman@yahoo.com">nasifzaman@yahoo.com</a>
        </div>
      </div>
    </primary-section>

    <!-- <primary-section texture="hexagons" title="Contact Me" subtitle="Hello, World.">
      <div class="block-content">
        <form name="contact" action="/" method="post" netlify>
          <input type="hidden" name="_gotcha">
          <input type="hidden" name="form-name" value="contact">
          <div class="field is-horizontal">
            <div class="field-label is-normal">
              <label class="label">From</label>
            </div>
            <div class="field-body">
              <div class="field">
                <p class="control is-expanded has-icons-left">
                  <input class="input" type="text" placeholder="Name" name="name">
                  <span class="icon is-small is-left">
                    <i class="mdi mdi-account"></i>
                  </span>
                </p>
              </div>
              <div class="field">
                <p class="control is-expanded has-icons-left">
                  <input class="input" type="email" placeholder="Email" name="email">
                  <span class="icon is-small is-left">
                    <i class="mdi mdi-at"></i>
                  </span>
                </p>
              </div>
            </div>
          </div>
          <div class="field is-horizontal">
            <div class="field-label is-normal">
              <label class="label">Subject</label>
            </div>
            <div class="field-body">
              <div class="field">
                <div class="control">
                  <input class="input" type="text" name="subject">
                </div>
              </div>
            </div>
          </div>
          <div class="field is-horizontal">
            <div class="field-label is-normal">
              <label class="label">Message</label>
            </div>
            <div class="field-body">
              <div class="field">
                <div class="control">
                  <textarea class="textarea" name="message"></textarea>
                </div>
              </div>
            </div>
          </div>
          <div class="field is-horizontal">
            <div class="field-label"></div>
            <div class="field-body">
              <div class="field">
                <div class="control">
                  <button class="button is-medium is-primary" type="submit">Send Message</button>
                </div>
              </div>
            </div>
          </div>
        </form>
      </div>
    </primary-section> -->
  </div>
</template>

<script>
import VueMarkdown from "vue-markdown";
import PrimarySection from "~/components/PrimarySection.vue";
import Gallery from "~/components/Gallery.vue";
import IconButtonLink from "~/components/IconButtonLink.vue";
import ImageBlockLink from "~/components/ImageBlockLink.vue";

export default {
  components: {
    VueMarkdown,
    PrimarySection,
    Gallery,
    IconButtonLink,
    ImageBlockLink
  },
  layout: "home"
};
</script>

<style lang="scss">
</style>
