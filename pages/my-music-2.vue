<template>
  <main class="my-music-2">
    <div class="my-music-2__jacket">
      <div class="my-music-2__image-genre">
        <img :src="topArtistImage">
        <div class="my-music-2__genre">
          <p class="my-music-2__header">Géneros favoritos</p>
          <ul>
            <li>{{ topGenre }}</li>
          </ul>
        </div>
      </div>
      <div class="my-music-2__artists-songs">
        <div class="my-music-2__artists">
          <p class="my-music-2__header">Artistas favoritos</p>
          <ul>
            <li
              v-for="artist in artists.items"
              :key="artist.name">
              {{ artist.name }}
            </li>
          </ul>
        </div>
        <div class="my-music-2__songs">
          <p class="my-music-2__header">Canciones favoritas</p>
          <ul>
            <li
              v-for="track in tracks.items"
              :key="track.name">
              {{ track.name }}
          </li></ul>
        </div>
      </div>
    </div>
    <div class="my-music-2__share">
      <h1>Comparte tu música</h1>
      <p class="my-music-2__share--description">
        Si llevas tiempo disfrutando de temazos,
        ¿por qué no lo compartes?
      </p>
      <p class="twitter-share-button">
        <a
          :href="`https://twitter.com/intent/tweet?text=${tweetText}&url=${tweetUrl}&via=${tweetVia}`"
          target="_blank"
        >
          <img src="~assets/images/twitter-icon.png">
        </a>
      </p>
    </div>
  </main>
</template>

<script>
export default {
    head() {
        return {
            title: 'Comparte tu música',
            meta: [
                {
                    hid: 'description',
                    name: 'description',
                    content:
                        'Comparte tus artistas y canciones favoritos de Wecodefy.',
                },
                { name: 'twitter:title', content: 'Wecodefy' },
                {
                    name: 'twitter:description',
                    content:
                        'Descubre tus artistas y canciones favoritos de Wecodefy',
                },
                {
                    name: 'twitter:image',
                    content: '~assets/images/wecodefy-logo.png',
                },
                { name: 'twitter:card', content: 'summary_large_image' },
            ],
            link: [
                {
                    rel: 'canonical',
                    href: 'https://github.com/cristinafsanz/taller-nuxt',
                },
            ],
        };
    },
    data() {
        return {
            tweetText: 'Descubre tus artistas y canciones favoritos en Wecodefy. Haz el taller de Nuxt en Wecodefest :)',
            tweetUrl: 'https://github.com/cristinafsanz/taller-nuxt',
            tweetVia: 'cristinafsanz',
        };
    },
    computed: {
        artists() {
            return this.$store.state.artistsYears;
        },
        topArtistImage() {
            return this.$store.state.topArtistImageYears;
        },
        tracks() {
            return this.$store.state.tracksYears;
        },
        topGenre() {
            return this.$store.state.topGenreYears;
        },
    },
};
</script>

<style scoped>
main {
    background-color: #b79cc9;
}
.my-music-2 {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}
/* Same width 2 items */
.my-music-2__jacket,
.my-music-2__share {
    margin-left: 1rem;
    margin-right: 1rem;
}
/* Jacket section */
.my-music-2__jacket {
    display: flex;
    flex-direction: column;
    background-color: #000;
    color: #b79cc9;
    padding: 1.5rem;
    font-size: 1.2em;
    line-height: 1.4em;
    align-items: center;
}
.my-music-2__image-genre {
    align-self: center;
}
.my-music-2__image-genre img {
    max-width: 200px;
}
.my-music-2 ul {
    padding: 0;
    list-style-type: none;
}
.my-music-2__header {
    font-size: 1.1em;
    font-weight: 600;
    margin-bottom: 0.75rem;
}
.my-music-2__songs {
    margin-top: 1.25rem;
}
.my-music-2__genre {
    margin-top: 1rem;
}
.my-music-2__genre li {
    font-size: 2em;
    font-weight: bold;
}
.my-music-2__artists {
    margin-top: 2rem;
}
.my-music-2__artists-songs {
    margin-left: 1.5rem;
}

/* Share section */
.my-music-2__share {
    color: #fff;
}
.my-music-2__share h1 {
    font-size: 3em;
    margin-top: 1rem;
    margin-bottom: 1rem;
}
.my-music-2__share .my-music-2__share--description {
    font-size: 1em;
    margin-bottom: 1rem;
}
.twitter-share-button {
    text-align: center;
}
@media (min-width: 1000px) {
    .my-music-2 {
        flex-direction: row;
    }
    .my-music-2__jacket,
    .my-music-2__share {
        flex-basis: 45%;
    }
    .my-music-2__jacket {
        flex-direction: row;
    }
    .my-music-2__image-genre {
        align-self: auto;
    }
    .my-music-2__share h1 {
        font-size: 6em;
    }
    .my-music-2__share .my-music-2__share--description {
        font-size: 1.5em;
    }
    .my-music-2__artists {
        margin-top: 0;
    }
}
@media (min-width: 1400px) {
    .my-music-2__jacket,
    .my-music-2__share {
        flex-basis: 33%;
        margin-left: 0;
        margin-right: 2rem;
    }
}
</style>
