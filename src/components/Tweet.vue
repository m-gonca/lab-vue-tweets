<template>
  <div className="tweet">
    <!-- <img
      :src="url"
      className="profile"
      alt="profile"
    /> -->
    <!-- <div className="body">
      <div className="top">
        <span className="user">
          <span className="name">{{name}}</span>
          <span className="handle">@{{user}}</span>
        </span>
        <span className="timestamp">{{date}}</span>
      </div> -->
      <!-- <p className="message">
        {{message}}
      </p>           -->
      <!-- <div className="actions">
        <i class="far fa-comment"></i>
        <i class="fas fa-retweet"></i>
        <i class="far fa-heart"></i>
        <i class="fas fa-share"></i>
      </div> -->

    <ProfileImage :image="user.image" />
    <div className="body">
      <div className="top">
        <User :userData="user" />
        <Timestamp :time="timestamp" />
    </div>
    <Message :message="message"/>
    <Actions/>
    <i class="fas fa-ellipsis-h"></i>
    </div>
  </div>
</template>

<script>
import ProfileImage from './ProfileImage.vue';
import User from './User.vue';
import Timestamp from './Timestamp.vue';
import Message from './Message.vue';
import Actions from './Actions.vue';


export default {
	name: "Tweet",
	// props: ["name", "user", "date", "message", "url"],
  components: { 
    ProfileImage,
    User,
    Timestamp,
    Message,
    Actions,
   },
  props: {
    user: Object,
    timestamp: String,
    message: String
  },

}
</script>

<style scoped>
a {
  color: #42b983;
}
</style>
