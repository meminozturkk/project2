<template>
  <div id="body">
    <div id="normalBody">
      <div id="navBar">
        <router-link to="/">
          <div id="ant">
            <img
              id="suudTitle"
              src="https://www.suudcollection.com/Uploads/EditorUploads/suud-image/logo.svg"
            />
          </div>
        </router-link>

        <ul id="navBarButtonsUL" class="container">
          <li>
            <router-link to="/productList">Çok satanlar</router-link>
          </li>
          <li>
            <router-link to="/productList">EN YENILER</router-link>
          </li>
          <li>
            <router-link to="/productList">GİYİM</router-link>
          </li>
          <li>
            <router-link to="/productList">Çanta</router-link>
          </li>
          <li>
            <router-link to="/productList">Aksesuar</router-link>
          </li>
          <li id="indirimLi">
            <router-link to="/productList">11.11 İNDİRİMLERİ</router-link>
          </li>
        </ul>

        <div id="navBarRightButtons">
          <ul id="navMenu">
            <li id="flag-icon">
              <a>
                <img src="../assets/sepetim.svg" />
              </a>
            </li>

            <li id="flag">
              <a>
                <img
                  src="https://cdn-icons-png.flaticon.com/512/175/175461.png"
                />
              </a>
            </li>

            <li id="flag"></li>

            <li id="flag">
              <a>
                <img
                  src="https://cdn-icons-png.flaticon.com/512/1077/1077035.png"
                />
              </a>
            </li>

            <li id="flag">
              <p>(0)</p>
            </li>
          </ul>
        </div>
      </div>
    </div>
    <div id="searchModeBody" style="display: none">
      <p id="searchModeSuud">SUUD</p>
      <form style="background-color: white" id="formSearch">
        <div id="searchDiv">
          <button type="button">
            <span>
              <img
                src="https://img.icons8.com/search"
                style="width: 30px; height: auto"
              />
            </span>
          </button>
          <input
            id="inputSearch"
            placeholder="Ürün, koleksiyon veya anahtar kelime ara"
          />
        </div>

        <ul class="searchUL">
          <li>
            <strong> Sizin İçin Tavsiyelerimiz </strong>
          </li>
          <li>
            <a href="#"> Çok Satanlar</a>
          </li>
          <li>
            <a href="#"> En Yeniler </a>
          </li>
          <li>
            <a href="#"> Giyim </a>
          </li>
          <li>
            <a href="#"> Aksesuar </a>
          </li>
          <li>
            <a href="#"> Çanta </a>
          </li>
          <li>
            <a href="#"> Ayakkabı </a>
          </li>
          <li id="SCMIndirimLi">
            <a href="#"> İndirim </a>
          </li>
        </ul>
      </form>
    </div>

    <cart-preview />
    <register />

    <router-view />
  </div>
</template>

<style scoped>
* {
  font-family: "Quicksand", sans-serif;
}
h1 {
  background-color: #fff;
  margin: auto;
}
body {
  height: auto;
  min-height: 1500px;
  width: 100%;
  max-width: 100%;
  background-color: #fff;
}
#normalBody {
  position: fixed;
  top: 0;
  height: auto;
  z-index: 100;
  /* min-height: 1500px; */
  padding-top: 0;
  padding-bottom: 0;
  width: 100%;
  max-width: 100%;
  background-color: #fff;
  margin: 10px;
  margin-bottom: 0;
  margin-top: 0;
  margin-left: 0;
}
#searchModeBody {
  height: auto;
  min-height: 1500px;
  width: 100%;
  max-width: 100%;
  background-color: #fff;
}
#navBar {
  width: 100%;
  height: auto;
  background-color: #fff;
  display: inline-flex;
  flex-direction: row;
}
#navBar a {
  position: relative;
  text-decoration: none;
  color: black;
  margin-bottom: 15px;
}
#navBar button {
  height: auto;
  position: relative;
  margin-left: 15%;
  margin-top: auto;
  margin-bottom: auto;
  background-color: white;
  border-style: none;
  border-bottom-style: solid;
  border-bottom: 1px solid;
  border-bottom-color: darkgrey;
  color: darkgrey;
  text-align: center;
}
#navBar button:hover {
  cursor: pointer;
}

#suudTitle {
  color: #000;
  width: 100px;
  margin-left: 35px;
  position: relative;
  cursor: pointer;
  margin-bottom: 2px;
}
#navBarButtonsUL {
  position: relative;
  text-decoration: none;
  list-style: none;
  display: inline-flex;
  flex-direction: row;
  margin-bottom: 2px;
}
#navBarButtonsUL li {
  margin-left: 17px;
  text-align: left;
  margin-top: auto;
  margin-bottom: auto;
  font-size: 16px;
  font-weight: bold;
}
#navBarButtonsUL li:hover {
  border-bottom: 2px solid black;
  cursor: pointer;
}
#navBarButtonsUL li a {
  text-transform: uppercase;
}
#indirimLi a {
  color: #bb0b0e;
  padding-left: 2px;
}
#searchDiv {
  width: 100%;
  padding-top: 5%;
  padding-left: 15%;
  display: flex;
  align-items: center;
}
#searchIcon img {
  width: 20px;
  height: 20px;
}
#inputSearch {
  width: 75%;
  position: relative;

  height: 3%;
  border-style: none;
  font-size: 25px;
  border-bottom-style: solid;
  background-color: #fff;
}
.searchUL {
  color: #000;
}
#searchModeBody {
  animation: fade 1.5s forwards;
}
@keyframes fade {
  from {
    opacity: 0;
  }
  to {
    opacity: 100%;
  }
}
#searchModeBody button {
  position: relative;
  color: darkgrey;
  width: auto;
  height: 3%;
  background-color: #fff;
  border-style: none;
}
#searchModeBody li {
  display: block;
  margin: auto;
  width: 85%;
  height: auto;
  text-align: left;
  font-size: 25px;
  padding-left: 15%;
}
#searchModeBody a {
  text-decoration: none;
  color: black;
}
#searchModeSuud {
  width: 85%;
  margin: auto;
  height: auto;
  background-color: #fff;
  text-align: left;
  padding-left: 15%;
  font-size: 50px;
}

#navBarRightButtons {
  position: relative;
  width: auto;
  height: auto;
  margin-top: auto;
  margin-bottom: auto;
}
#navMenu {
  width: auto;
  height: auto;
  margin-bottom: auto;
  margin-top: auto;
  position: relative;
  text-decoration: none;
  list-style: none;
  display: inline-flex;
  flex-direction: row;
}
#navMenu li {
  position: relative;
  width: auto;
  height: auto;
  padding-left: 20px;
  padding-right: 20px;
  border-left-style: solid;
  border-left-width: 1px;
  border-left-color: #d3d3d3;
  display: inline-flex;
  flex-direction: row;
}
#navMenu img {
  width: 20px;
  height: 20px;
}
#navMenu li:hover {
  cursor: pointer;
}
#navMenu a {
  position: relative;
  margin-top: auto;
  margin-bottom: auto;
}
#navMenu p {
  position: relative;
  margin-left: 5px;
  margin-top: auto;
  margin-bottom: auto;
  height: auto;
  width: auto;
}
#searchModeExitButton img {
  position: relative;
  width: 20px;
  height: 20px;
  margin-bottom: auto;
  margin-top: auto;
}
#searchModeExitButton img:hover {
  cursor: pointer;
}
#searchModeExitButton {
  text-align: right;
  padding-right: 5%;
}
#ant {
  margin-top: 35px;
  size: 111px * 33px;
}
</style>
