<template>
  <div class="meu-componente">
    <div class="LoginBlock">
      <h1>Login</h1>
      <form @submit.prevent>
        <input type="text" placeholder="Email" />
        <input
          :type="showPassword ? 'text' : 'password'"
          placeholder="Password"
        />
        <div class="ShowPs">
          <input type="checkbox" class="ShowPassword" v-model="showPassword" />
          <p>show password</p>
        </div>
        <button type="submit">Login</button>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: "MeuComponente",
  data() {
    return {
      showPassword: false,
    };
  },
};
</script>

<style>
body {
  font-family: "Freckle Face", system-ui;
  overflow: hidden;
  margin: 0;
  background-color: rgb(0, 0, 0);
  background-image: url("../assets/Background.jpeg");
  background-size: cover;
  background-repeat: no-repeat;
  background-attachment: fixed;
}
</style>

<style scoped>
.meu-componente {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  width: 100vw;
  margin-top: -6%;
}

.LoginBlock {
  height: 500px;
  width: 400px;
  background-color: rgb(45, 0, 119, 0.8);
  border-radius: 15px;
  border: 1px solid rgba(25, 25, 25, 0.8);
  box-shadow: 0px 20px 40px 10px rgba(0, 0, 0, 0.9);
  backdrop-filter: blur(5px);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 40px;
}

& h1 {
  background-color: rgb(50, 0, 150, 0.7);
  color: white;
  font-family: "Freckle Face", system-ui;
  font-size: 36px;
  font-weight: 300;
  height: 60px;
  box-shadow: 0px 15px 10px 5px rgb(0, 0, 0, 0.5);
  width: 90%;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 0;
  border: 2px solid rgba(0, 0, 0, 0.5);
  border-radius: 100px;
}

& form {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 80%;
  gap: 30px;
}

& input {
  font-family: "Freckle Face", system-ui;
  width: 100%;
  height: 40px;
  background-color: rgba(0, 0, 0, 0.3);
  border: 1px solid rgba(255, 255, 255, 0.3);
  border-radius: 8px;
  padding: 0 15px;
  color: white;
  font-size: 16px;
  box-sizing: border-box;
}
.ShowPs {
  display: flex;
  text-align: center;
  justify-content: center;
  align-items: center;
  gap: 10px;
}
.ShowPassword {
  padding: 0px 0px;
  border: none;
  height: 30px;
  width: 30px;
  transition: all 0.3s;
}
.ShowPassword:hover {
  opacity: 0.6;
}
p {
  font-family: "Freckle Face", system-ui;
  color: white;
}

.LoginBlock input::placeholder {
  color: rgba(255, 255, 255, 0.6);
}

.LoginBlock input:focus {
  outline: none;
  border-color: rgb(20, 180, 60);
}

.LoginBlock button {
  font-family: "Freckle Face", system-ui;
  width: 100%;
  height: 45px;
  border: none;
  border-radius: 8px;
  background-color: white;
  color: #3a0ca3;
  font-size: 18px;
  font-weight: bold;
  cursor: pointer;
  transition: transform 0.5s ease;
}

.LoginBlock button:hover {
  transform: scale(1.03);
}
</style>
