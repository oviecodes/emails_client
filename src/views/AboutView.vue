<template>
  <div class="about">
    <div>

      <h1 class="heading">
        About UoRos
      </h1>

      <p class="desc_text">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Esse maiores velit molestias assumenda numquam eligendi. Perferendis pariatur, eligendi at nostrum odio ducimus quod consequatur dignissimos culpa magni commodi, quo esse!
      </p>

      <h1 class="heading">
        What we do
      </h1>

      <p class="desc_text">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Esse maiores velit molestias assumenda numquam eligendi. Perferendis pariatur, eligendi at nostrum odio ducimus quod consequatur dignissimos culpa magni commodi, quo esse!

        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Placeat voluptatibus officia atque fuga nesciunt rem iste ab saepe ducimus, praesentium soluta quis temporibus, tempora voluptas facere quos reprehenderit beatae in!
      </p>

      <h1 class="heading">
        Join our mailing list
      </h1>

      <p class="desc_text">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Delectus eum assumenda dolor laudantium sed temporibus nulla sunt dicta voluptatibus asperiores harum officiis, at, quibusdam beatae corrupti. Suscipit placeat modi corrupti!
      </p>

      <div>
        <form action="" @submit="signUpToMail">
          <p>{{ error }}</p>
          <input type="email" class="email_input" name="email" placeholder="Email address" id="" v-model="email">
          <input type="submit" class="email_submit" value="Sign up">
        </form>
      </div>
    </div>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }

  .heading {
    /* margin: 10px 0; */
    font-weight: 700;
  }

  .desc_text {
    margin: 0 0 15px 0;
  }

  .email_input {
    padding: 12px 10px;
    font-size: 16px;
    border: none;
    background: rgb(232, 240, 254)
  }

  .email_submit {
    background-color: hsla(160, 100%, 37%, 1); /* Green */
    border: none;
    color: white;
    padding: 12px 10px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 0 5px;
  }

}
</style>

<script>
import axios from 'axios'

export default {

  data() {
    return {
      email: '',
      error: ''
    }
  },

  methods: {

    async signUpToMail(e) {
      e.preventDefault()

      if(!this.email) return this.error = `Enter an email address`

      const data = {
        data: {email: this.email}
      }

      console.log('Email', this.email)
      try {

        await axios(`http://localhost:1337/api/mailing-lists`, {
          method: 'POST',
          data
        })
        
      } catch (error) {

        console.log(error)
        
      }
      
      this.email = ''
      this.error = ''
    }

  }
  
}
</script>