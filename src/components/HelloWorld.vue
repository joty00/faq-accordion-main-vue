<template>
  <main class="principal">
    <div class="head">
      <svg class="star" xmlns="http://www.w3.org/2000/svg" width="40" height="41" fill="none" viewBox="0 0 40 41"><path fill="#AD28EB" d="M37.5 20.5a2.467 2.467 0 0 1-1.64 2.344l-9.913 3.604-3.603 9.911a2.5 2.5 0 0 1-4.688 0l-3.604-9.922-9.911-3.593a2.5 2.5 0 0 1 0-4.688l9.921-3.604 3.594-9.911a2.5 2.5 0 0 1 4.688 0l3.604 9.921 9.911 3.594A2.467 2.467 0 0 1 37.5 20.5Z"/></svg>
      <h1 class="title">
        FAQs
      </h1>
    </div>
    <div class="questions">
      <div class="question_1">
        <div class="question-header">
          <div class="ques" @click="toggleAnswer(1)">
            <p>
              What is Frontend Mentor, and how will it help me?
            </p>
            <span class="plus-icon" v-if="!isOpen[1]"><svg xmlns="http://www.w3.org/2000/svg" width="30" height="31" fill="none" viewBox="0 0 30 31"><path fill="#AD28EB" d="M15 3.313A12.187 12.187 0 1 0 27.188 15.5 12.203 12.203 0 0 0 15 3.312Zm4.688 13.124h-3.75v3.75a.938.938 0 0 1-1.876 0v-3.75h-3.75a.938.938 0 0 1 0-1.875h3.75v-3.75a.938.938 0 0 1 1.876 0v3.75h3.75a.938.938 0 0 1 0 1.876Z"/></svg></span>
            <span class="minus-icon" v-else><svg xmlns="http://www.w3.org/2000/svg" width="30" height="31" fill="none" viewBox="0 0 30 31"><path fill="#301534" d="M15 3.313A12.187 12.187 0 1 0 27.188 15.5 12.2 12.2 0 0 0 15 3.312Zm4.688 13.124h-9.375a.938.938 0 0 1 0-1.875h9.374a.938.938 0 0 1 0 1.876Z"/></svg></span>
          </div>
        </div>
        <div class="answer" v-show="isOpen[1]">
          <p>
            Frontend Mentor offers realistic coding challenges to help developers improve their frontend coding skills with projects in HTML, CSS, and JavaScript. It's suitable for all levels and ideal for portfolio building.
          </p>
        </div>
        <hr>
      </div>

      <div class="question_2">
        <div class="ques" @click="toggleAnswer(2)">
          <p>
            Is Frontend Mentor free?
          </p>
          <span class="plus-icon"  v-if="!isOpen[2]"><svg xmlns="http://www.w3.org/2000/svg" width="30" height="31" fill="none" viewBox="0 0 30 31"><path fill="#AD28EB" d="M15 3.313A12.187 12.187 0 1 0 27.188 15.5 12.203 12.203 0 0 0 15 3.312Zm4.688 13.124h-3.75v3.75a.938.938 0 0 1-1.876 0v-3.75h-3.75a.938.938 0 0 1 0-1.875h3.75v-3.75a.938.938 0 0 1 1.876 0v3.75h3.75a.938.938 0 0 1 0 1.876Z"/></svg></span>
          <span class="minus-icon" v-else><svg xmlns="http://www.w3.org/2000/svg" width="30" height="31" fill="none" viewBox="0 0 30 31"><path fill="#301534" d="M15 3.313A12.187 12.187 0 1 0 27.188 15.5 12.2 12.2 0 0 0 15 3.312Zm4.688 13.124h-9.375a.938.938 0 0 1 0-1.875h9.374a.938.938 0 0 1 0 1.876Z"/></svg></span>
        </div>
        <div class="answer" v-show="isOpen[2]">
          <p>
            Yes, Frontend Mentor offers both free and premium coding challenges, with the free 
            option providing access to a range of projects suitable for all skill levels.
          </p>
        </div>
        <hr>
      </div>

      <div class="question_3">
        <div class="ques" @click="toggleAnswer(3)">
          <p>
            Can I use Frontend Mentor projects in my portfolio?
          </p>
          <span class="plus-icon"  v-if="!isOpen[3]"><svg xmlns="http://www.w3.org/2000/svg" width="30" height="31" fill="none" viewBox="0 0 30 31"><path fill="#AD28EB" d="M15 3.313A12.187 12.187 0 1 0 27.188 15.5 12.203 12.203 0 0 0 15 3.312Zm4.688 13.124h-3.75v3.75a.938.938 0 0 1-1.876 0v-3.75h-3.75a.938.938 0 0 1 0-1.875h3.75v-3.75a.938.938 0 0 1 1.876 0v3.75h3.75a.938.938 0 0 1 0 1.876Z"/></svg></span>
          <span class="minus-icon" v-else><svg xmlns="http://www.w3.org/2000/svg" width="30" height="31" fill="none" viewBox="0 0 30 31"><path fill="#301534" d="M15 3.313A12.187 12.187 0 1 0 27.188 15.5 12.2 12.2 0 0 0 15 3.312Zm4.688 13.124h-9.375a.938.938 0 0 1 0-1.875h9.374a.938.938 0 0 1 0 1.876Z"/></svg></span>
        </div>
        <div class="answer" v-show="isOpen[3]">
          <p>
            Yes, you can use projects completed on Frontend Mentor in your portfolio. It's an excellent
            way to showcase your skills to potential employers!
          </p>
        </div>
        <hr>
      </div>

      <div class="question_4">
        <div class="ques" @click="toggleAnswer(4)">
          <p>
            How can I get help if I'm stuck on a challenge?
          </p>
          <span class="plus-icon" v-if="!isOpen[4]"><svg xmlns="http://www.w3.org/2000/svg" width="30" height="31" fill="none" viewBox="0 0 30 31"><path fill="#AD28EB" d="M15 3.313A12.187 12.187 0 1 0 27.188 15.5 12.203 12.203 0 0 0 15 3.312Zm4.688 13.124h-3.75v3.75a.938.938 0 0 1-1.876 0v-3.75h-3.75a.938.938 0 0 1 0-1.875h3.75v-3.75a.938.938 0 0 1 1.876 0v3.75h3.75a.938.938 0 0 1 0 1.876Z"/></svg></span>
          <span class="minus-icon" v-else><svg xmlns="http://www.w3.org/2000/svg" width="30" height="31" fill="none" viewBox="0 0 30 31"><path fill="#301534" d="M15 3.313A12.187 12.187 0 1 0 27.188 15.5 12.2 12.2 0 0 0 15 3.312Zm4.688 13.124h-9.375a.938.938 0 0 1 0-1.875h9.374a.938.938 0 0 1 0 1.876Z"/></svg></span>
        </div>
        <div class="answer" v-show="isOpen[4]">
          <p>
            The best place to get help is inside Frontend Mentor's Discord community. There's a help 
            channel where you can ask questions and seek support from other community members.
          </p>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  data() {
    return {
      isOpen: {
        1: false,
        2: false,
        3: false,
        4: false,
      },
    };
  },
  methods: {
    toggleAnswer(questionNumber) {
      this.isOpen[questionNumber] = !this.isOpen[questionNumber];
    },
    
  },
};
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Work+Sans:wght@400;600;700&display=swap');
  body {
    font-family: 'Work Sans', sans-serif;
    margin: 0;
    background: hsla(293, 16%, 49%, 0.306);
    background-image: url(../../public/background-pattern-mobile.svg);
    background-repeat: no-repeat;
    background-size: contain;
    display: flex;
    flex-direction: column;
    align-items: center;
    height: 100vh;
  }
  .principal {
    background: hsl(0, 0%, 100%);
    border-radius: 10px;
    width: 340px;
    position: fixed;
    top: 50%;
    left: 50%;
    margin-top: -260px;
    margin-left: -170px;
    max-height: 80vh;
    overflow-y: scroll; 
  }

  .head {
    display: flex;
  }

  .star {
    margin: 30px 20px 0 20px;

  }

  .head h1 {
    color: hsl(292, 42%, 14%);
    
  }

  svg {
    height: 25px;
  }

  .ques {
    display: flex;
    justify-content: space-around;
    margin-left: 10px;
    width: 320px;
  }

  .ques p {
    font-weight: 600;
    font-size: 16px;
    width: 260px;
    cursor: pointer;
  }

  .ques p:hover {
    color: rgb(173, 40, 235);;
  }

  .ques svg {
    cursor: pointer;
  }

  .plus-icon, .minus-icon {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  hr {
    width: 300px;
    border-color: hsla(293, 16%, 49%, 0.098);
  }

  .answer {
    margin-left: 20px;
    color: hsl(292, 16%, 49%);
    width: 300px;
    font-size: 15.5px;
  }

  @media screen and (min-width: 740px) {
    .principal {
      width: 560px;
      margin-top: -270px;
      margin-left: -290px;
    }

    .ques {
      width: 490px;
      margin-left: 40px;
      margin-right: 20px;
      margin-bottom: 30px;
    }

    .ques p {
      width: 470px;
    }

    body {
      background-size: auto;
      background-image: url(../../public/background-pattern-desktop.svg);
    }

    .title {
      font-size: 50px;
    }

    .star {
      height: 50px;
      margin: 40px 30px 0 30px;
    }

    .minus-icon, .plus-icon {
      height: 45px;
    }

    .answer {
      width: 500px;
      margin-left: 40px;
    }
  }
</style>