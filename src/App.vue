<script>
export default {
  data() {
    return {
      genres: [
        { id: 1, name: "Drama" },
        { id: 2, name: "Comédia" },
        { id: 3, name: "Ação" },
        { id: 4, name: "Romance" },
      ],
    };
    async created() {
      const url = `https://api.themoviedb.org/3/genre/movie/list?api_key=e459257500dba9d31f1002e2efdc21ac&language=pt-br`
      const { data } = await axios.get(url)
      this.genres = data
    }
  },
};
</script>
<template>
  <header>
    <div class="nome text-center">
      <h1>COPIAFLIX</h1>
    </div>

    <nav class="navbar navbar-expand-lg navbar-light cor1">
      <div class="container-fluid">
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarScroll"
          aria-controls="navbarScroll"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarScroll">
          <ul
            class="navbar-nav me-auto my-2 my-lg-0 navbar-nav-scroll"
            style="--bs-scroll-height: 100px"
          >
            <li class="nav-item">
              <a class="nav-link" aria-current="page" href="#">Home</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Filmes</a>
            </li>
            <li class="nav-item dropdown">
              <a
                class="nav-link dropdown-toggle"
                href="#"
                id="navbarScrollingDropdown"
                role="button"
                data-bs-toggle="dropdown"
                aria-expanded="true"
              >
                Generos
              </a>
              <ul
                class="dropdown-menu"
                aria-labelledby="navbarScrollingDropdown"
              >
                <li v-for="genre of genres" :key="genre.id">
                  <a class="dropdown-item" href="#Filmes">{{ genre.name }}</a>
                </li>
                <li v-for=""></li>
                <!-- <li><a class="dropdown-item" href="/about">Séries</a></li> -->
                <!-- <li> -->
                <!-- <a class="dropdown-item" href="#Documentario">Documentario</a> -->
                <!-- </li> -->
                <!-- <li><hr class="dropdown-divider" /></li> -->
                <!-- <li><a class="dropdown-item" href="#">Opção</a></li> -->
              </ul>
            </li>
            <li class="nav-item">
              <a class="nav-link">Planos</a>
            </li>
          </ul>
          <form class="d-flex">
            <input
              class="form-control me-2"
              type="search"
              placeholder="Search"
              aria-label="Search"
            />
            <button class="btn btn-outline-success" type="submit">
              Search
            </button>
          </form>
        </div>
      </div>
    </nav>
  </header>
  <main>
    <Routerlink></Routerlink>
    <div
      id="carouselExampleIndicators"
      class="carousel slide"
      data-bs-ride="carousel"
    >
      <div class="carousel-indicators">
        <button
          type="button"
          data-bs-target="#carouselExampleIndicators"
          data-bs-slide-to="0"
          class="active"
          aria-current="true"
          aria-label="Slide 1"
        ></button>
        <button
          type="button"
          data-bs-target="#carouselExampleIndicators"
          data-bs-slide-to="1"
          aria-label="Slide 2"
        ></button>
        <button
          type="button"
          data-bs-target="#carouselExampleIndicators"
          data-bs-slide-to="2"
          aria-label="Slide 3"
        ></button>
      </div>
      <div class="carousel-inner">
        <div class="carousel-item active">
          <img
            src="https://prod-ripcut-delivery.disney-plus.net/v1/variant/disney/E57BA22516F76D93CF581C74E35AF58A3E317AF798D1EACE47CC210F3A5F5A65/scale?width=2880&aspectRatio=1.78&format=jpeg"
            width="1600"
            height="600"
          />
        </div>
        <div class="carousel-item">
          <img
            src="https://tracklist.com.br/wp-content/uploads/2021/11/1636043728095981-0.jpg"
            width="1600"
            height="600"
          />
        </div>
        <div class="carousel-item">
          <img
            src="https://t.ctcdn.com.br/NN8ouhv1G2bQdv5zfOPTR4JjXyY=/1400x788/smart/i327740.jpeg"
            width="1600"
            height="600"
          />
        </div>
      </div>
      <button
        class="carousel-control-prev"
        type="button"
        data-bs-target="#carouselExampleIndicators"
        data-bs-slide="prev"
      >
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Previous</span>
      </button>
      <button
        class="carousel-control-next"
        type="button"
        data-bs-target="#carouselExampleIndicators"
        data-bs-slide="next"
      >
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Next</span>
      </button>
    </div>

    <br />

    <div class="container text-light" id="Filmes">
      <h2>FILMES</h2>
    </div>

    <div class="container">
      <div class="row">
        <div class="col-md-3">
          <img
            src="Imagens e plugs/Rambo.jpg_t=20210728222416"
            width="600"
            height="400"
          />
        </div>
        <div class="col-md-3">
          <img src="Imagens e plugs/The bat.jpg" width="600" height="400" />
        </div>
        <div class="col-md-3">
          <img
            src="Imagens e plugs/The_Dark_Knight.jpg"
            width="600"
            height="400"
          />
        </div>
        <div class="col-md-3">
          <img
            src="Imagens e plugs/Rambo.jpg_t=20210728222416"
            width="600"
            height="400"
          />
        </div>
      </div>
    </div>

    <br /><br />

    <div class="container text-light" id="Series">
      <h2>SÉRIES</h2>
    </div>

    <div class="container">
      <div class="row">
        <div class="col-md-3">
          <img
            src="Imagens e plugs/Infinit dark.jpg"
            width="600"
            height="400"
          />
        </div>

        <div class="col-md-3">
          <img
            src="Imagens e plugs/Supernatural_temporada_10_Poster.png"
            width="600"
            height="400"
          />
        </div>

        <div class="col-md-3">
          <img src="Imagens e plugs/Grey.jpg" width="600" height="400" />
        </div>

        <div class="col-md-3">
          <img src="Imagens e plugs/Lucifer.jpg" width="600" height="400" />
        </div>
      </div>
    </div>

    <br /><br />

    <div class="container text-light" id="Documentario">
      <h2>Documentarios</h2>
    </div>

    <div class="container">
      <div class="row">
        <div class="col">
          <img
            src="Imagens e plugs/The_Dark_Knight.jpg"
            width="600"
            height="400"
          />
        </div>

        <div class="col-md-3">
          <img src="Imagens e plugs/Doc2.jpg" width="600" height="400" />
        </div>

        <div class="col-md-3">
          <img
            src="Imagens e plugs/The_Dark_Knight.jpg"
            width="600"
            height="400"
          />
        </div>

        <div class="col-md-3">
          <img src="Imagens e plugs/Doc2.jpg" width="600" height="400" />
        </div>
      </div>
    </div>
  </main>
</template>
<style>
@import "@/assets/main.css";
@import "@/assets/base.css";
</style>
