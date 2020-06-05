<script context="module">
    // TODO: implement API to use this code
    /*
    export async function preload() {
        let data = {};
        const response = await this.fetch()
        data = await response.json();
        return { data };
    }
     */
</script>

<script>
    import {onMount} from 'svelte';
    import Header from '../components/Header.svelte'
    import Main from '../components/Main.svelte'
    import TimeLine from '../components/TimeLine.svelte'
    import Sidebar from '../components/Sidebar.svelte'

    let data = {
      "user": {
        "nickname": "ziker",
        "name": "Alejandro Cortez"
      },
      "posts": [
        {
          "username": "pelusi_official",
          "location": "Ciudad de México, México",
          "avatar": "https://ziker.s3.us-east-2.amazonaws.com/pelu.jpg",
          "photo":  "https://ziker.s3.us-east-2.amazonaws.com/pelu_bb.jpg",
          "like": false,
          "bookmark": false,
          "postComment": "Siendo un sultan",
          "comments": [
            {
              "id": 123234535,
              "text": "Hola Elmo",
              "username": "Crispeta"
            },
            {
              "id": 1232322312,
              "text": "¡Hola!",
              "username": "Dollarsin"
            }
          ]
        },
        {
          "username": "pelusi_official",
          "location": "Ciudad de México, México",
          "avatar": "https://ziker.s3.us-east-2.amazonaws.com/pelu.jpg",
          "photo":  "https://ziker.s3.us-east-2.amazonaws.com/pelu_bb.jpg",
          "like": false,
          "bookmark": false,
          "postComment": "Siendo un sultan",
          "comments": [
            {
              "id": 123234535,
              "text": "Elmito",
              "username": "ziker"
            }
          ]
        },
        {
          "username": "pelusi_official",
          "location": "Ciudad de México, México",
          "avatar": "https://ziker.s3.us-east-2.amazonaws.com/pelu.jpg",
          "photo":  "https://ziker.s3.us-east-2.amazonaws.com/pelu_bb.jpg",
          "like": false,
          "bookmark": false,
          "postComment": "Siendo un sultan",
          "comments": []
        },
        {
          "username": "pelusi_official",
          "location": "Ciudad de México, México",
          "avatar": "https://ziker.s3.us-east-2.amazonaws.com/pelu.jpg",
          "photo":  "https://ziker.s3.us-east-2.amazonaws.com/pelu_bb.jpg",
          "like": false,
          "bookmark": false,
          "postComment": "Un hueso para la dieta",
          "comments": []
        },
        {
          "username": "pelusi_official",
          "location": "Ciudad de México, México",
          "avatar": "https://ziker.s3.us-east-2.amazonaws.com/pelu.jpg",
          "photo":  "https://ziker.s3.us-east-2.amazonaws.com/pelu_bb.jpg",
          "like": false,
          "bookmark": false,
          "postComment": "Siendo un sultan",
          "comments": []
        },
        {
          "username": "pelusi_official",
          "location": "Ciudad de México, México",
          "avatar": "https://ziker.s3.us-east-2.amazonaws.com/pelu.jpg",
          "photo":  "https://ziker.s3.us-east-2.amazonaws.com/pelu_bb.jpg",
          "like": false,
          "bookmark": false,
          "postComment": "Siendo un sultan",
          "comments": []
        },
        {
          "username": "pelusi_official",
          "location": "Ciudad de México, México",
          "avatar": "https://ziker.s3.us-east-2.amazonaws.com/pelu.jpg",
          "photo":  "https://ziker.s3.us-east-2.amazonaws.com/pelu_bb.jpg",
          "like": false,
          "bookmark": false,
          "postComment": "A dormir",
          "comments": []
        },
        {
          "username": "pelusi_official",
          "location": "Ciudad de México, México",
          "avatar": "https://ziker.s3.us-east-2.amazonaws.com/pelu.jpg",
          "photo":  "https://ziker.s3.us-east-2.amazonaws.com/pelu_bb.jpg",
          "like": false,
          "bookmark": false,
          "postComment": "Siendo un sultan",
          "comments": []
        },
        {
          "username": "pelusi_official",
          "location": "Ciudad de México, México",
          "avatar": "https://ziker.s3.us-east-2.amazonaws.com/pelu.jpg",
          "photo":  "https://ziker.s3.us-east-2.amazonaws.com/pelu_bb.jpg",
          "like": false,
          "bookmark": false,
          "postComment": "Siendo un sultan",
          "comments": []
        }
      ]
    };
    /*
    const API_URL = 'https://us-central1-pugstagram-co.cloudfunctions.net/data';

    onMount(async () => {
        const response = await fetch(API_URL)
        data =  await response.json();
    })*/

</script>

<svelte:head>
  <title>Pelusigram</title>
</svelte:head>

<Main>
    <TimeLine posts={data.posts} />
    <Sidebar {...data.user} />
</Main>
