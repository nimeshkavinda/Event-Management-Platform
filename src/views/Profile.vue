<template>
  <div class="profile">
    <mdb-container fluid class="text-left">
      <mdb-row class="mx-5 my-5">
        <mdb-jumbotron
          class="mb-0 text-center hoverable p-4 mx-5"
          style="border-radius: 0.5em;"
        >
          <mdb-row>
            <mdb-col md="3" offsetMd="1" class="m-3">
              <mdb-avatar class="mx-auto white">
                <img
                  src="https://mdbootstrap.com/img/Photos/Avatars/img%20(9).jpg"
                  class="rounded-circle img-fluid"
                />
              </mdb-avatar>
            </mdb-col>
            <mdb-col md="8" class="text-md-left ml-3 mt-3">
              <a href="#!" class="green-text">
                <h3 class="h3 light-green-text" v-if="isMorning()">
                  Good Morning
                </h3>
                <h3 class="h3 light-green-text" v-else>
                  Good Afternoon
                </h3>
              </a>
              <h1 class="h1 mb-3 font-weight-bold">Nimesh Kavinda</h1>
              <mdb-icon fab icon="facebook-f" size="1x" class="mr-3" />
              <mdb-icon fab icon="instagram" size="1x" class="mr-3" />
              <mdb-icon fab icon="twitter" size="1x" class="mr-3" />
              <mdb-icon fab icon="linkedin" size="1x" class="mr-3" />
              <mdb-icon fab icon="github" size="1x" />

              <mdb-row>
                <mdb-col col="12" class="mt-3">
                  <p class="font-weight-bold">Bio</p>
                  <p class="font-weight-normal">
                    Sed ut perspiciatis unde omnis iste natus error sit
                    voluptatem accusantium doloremque, totam rem aperiam, eaque
                    ipsa quae ab illo inventore veritatis et quasi architecto
                    beatae vitae dicta sunt explicabo. Nemo enim ipsam
                    voluptatem quia voluptas sit aspernatur.
                  </p>
                </mdb-col>
              </mdb-row>

              <mdb-row>
                <mdb-col lg="6" class="mt-3">
                  <p class="font-weight-bold">Personal Information</p>
                </mdb-col>
                <mdb-col lg="6" class="mt-3">
                  <p class="font-weight-bold">Contact Information</p>
                </mdb-col>
              </mdb-row>

              <mdb-btn color="light-green" style="border-radius:1em;"
                >Edit Profile</mdb-btn
              >
            </mdb-col>
          </mdb-row>
        </mdb-jumbotron>
      </mdb-row>
      <mdb-row class="mx-5">
        <mdb-col md="5" class="mx-5">
          <p class="h3 blue-text font-weight-bold">
            Registered Events
          </p>
        </mdb-col>
      </mdb-row>
      <mdb-row class="mx-5">
        <mdb-col lg="6" class="mx-5">
          <p class="h3 blue-text font-weight-bold">
            Attended Events
          </p>
        </mdb-col>
        <mdb-col lg="6" class="mx-5">
          <a class="h6 blue-text font-weight-bold">
            See All
          </a>
        </mdb-col>
      </mdb-row>
    </mdb-container>
  </div>
</template>

<script>
import { mdbJumbotron, mdbRow, mdbCol, mdbBtn, mdbIcon } from "mdbvue";
export default {
  name: "JumbotronPage",
  components: {
    mdbJumbotron,
    mdbRow,
    mdbCol,
    mdbBtn,
    mdbIcon,
  },
  methods: {
    isMorning() {
      return new Date().getHours() < 12 ? true : false;
    },
  },
};
</script>
