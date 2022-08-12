<template>
  <div class="jobs">
    <h3>Jobs</h3>
    <div class="def" v-for="job in jobs" :key="job.id">
        <router-link :to="{ name: 'JobDetails', params: { id: job.id }}">
            <h4>{{ job.title }}</h4>
        </router-link>
    </div>
  </div>
</template>

<script>
export default {
    name: 'jobs',
    components: {},
    data() {
        return {
            jobs: [
                { title: 'UX Designer', id:1, detail: 'Pretty Good UX and UI designer'},
                { title: 'Front-End Developer', id:2, detail: 'Excelent Frond end Developer'},
                { title: 'Web Developer', id:3, detail: 'Really Good designs'}
            ]
        }
    }
}
</script>

<style>

 h3 {
    font-size: 30px;
    font-weight: 500;
    margin: 10px 30%;
    padding: 10px 20px;
    background: #277351;
    color: #ffffff;
    border-radius: 6px;
 }
 .def {
    align-items: center;
    justify-content: center;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
 }
 .def a {
    text-decoration: none;
    color: #454545;
    transition: 0.4s;
    background: #d9d9d9;
    border-radius: 7px;
    margin: 5px 20px;
    max-width: 400px;
    width:100%;
 }
 .def a:hover {
    background: #6c6c6c;
    color: #ffffff;
 }
</style>