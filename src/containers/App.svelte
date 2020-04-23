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
          "avatar": "https://scontent-qro1-1.xx.fbcdn.net/v/t1.0-9/44379866_10217113262846167_1434682057987981312_o.jpg?_nc_cat=106&_nc_sid=84a396&_nc_eui2=AeGJQNP9W7eKOxd27lrSwlomxYFVydwut2bFgVXJ3C63ZvWaaYmVmF9SpckSzn_xhQQ&_nc_ohc=rZNW3v75LIMAX8XrtOR&_nc_ht=scontent-qro1-1.xx&oh=03f6920c10f08f5ff0b6f1c2755a5fd3&oe=5EC7D2E5",
          "photo":  "https://scontent-qro1-1.xx.fbcdn.net/v/t1.0-9/1947407_10203253965412393_1800977331_n.jpg?_nc_cat=100&_nc_sid=d2e176&_nc_eui2=AeFqKFYxM1UaAZ8Os_mjK04bqXt7zwRCX8epe3vPBEJfx3HkTSBHOrnNlWTR0tzUWdo&_nc_ohc=G60Yb2FAC5cAX_AZHfZ&_nc_ht=scontent-qro1-1.xx&oh=9a1e9ce90008b2a8006348df9fdfc6eb&oe=5EC5581E",
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
          "avatar": "https://scontent-qro1-1.xx.fbcdn.net/v/t1.0-9/44379866_10217113262846167_1434682057987981312_o.jpg?_nc_cat=106&_nc_sid=84a396&_nc_eui2=AeGJQNP9W7eKOxd27lrSwlomxYFVydwut2bFgVXJ3C63ZvWaaYmVmF9SpckSzn_xhQQ&_nc_ohc=rZNW3v75LIMAX8XrtOR&_nc_ht=scontent-qro1-1.xx&oh=03f6920c10f08f5ff0b6f1c2755a5fd3&oe=5EC7D2E5",
          "photo":  "https://scontent-qro1-1.xx.fbcdn.net/v/t1.0-9/1947407_10203253965412393_1800977331_n.jpg?_nc_cat=100&_nc_sid=d2e176&_nc_eui2=AeFqKFYxM1UaAZ8Os_mjK04bqXt7zwRCX8epe3vPBEJfx3HkTSBHOrnNlWTR0tzUWdo&_nc_ohc=G60Yb2FAC5cAX_AZHfZ&_nc_ht=scontent-qro1-1.xx&oh=9a1e9ce90008b2a8006348df9fdfc6eb&oe=5EC5581E",
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
          "avatar": "https://scontent-qro1-1.xx.fbcdn.net/v/t1.0-9/44379866_10217113262846167_1434682057987981312_o.jpg?_nc_cat=106&_nc_sid=84a396&_nc_eui2=AeGJQNP9W7eKOxd27lrSwlomxYFVydwut2bFgVXJ3C63ZvWaaYmVmF9SpckSzn_xhQQ&_nc_ohc=rZNW3v75LIMAX8XrtOR&_nc_ht=scontent-qro1-1.xx&oh=03f6920c10f08f5ff0b6f1c2755a5fd3&oe=5EC7D2E5",
          "photo":  "https://scontent-qro1-1.xx.fbcdn.net/v/t1.0-9/1947407_10203253965412393_1800977331_n.jpg?_nc_cat=100&_nc_sid=d2e176&_nc_eui2=AeFqKFYxM1UaAZ8Os_mjK04bqXt7zwRCX8epe3vPBEJfx3HkTSBHOrnNlWTR0tzUWdo&_nc_ohc=G60Yb2FAC5cAX_AZHfZ&_nc_ht=scontent-qro1-1.xx&oh=9a1e9ce90008b2a8006348df9fdfc6eb&oe=5EC5581E",
          "like": false,
          "bookmark": false,
          "postComment": "Siendo un sultan",
          "comments": []
        },
        {
          "username": "pelusi_official",
          "location": "Ciudad de México, México",
          "avatar": "https://scontent-qro1-1.xx.fbcdn.net/v/t1.0-9/44379866_10217113262846167_1434682057987981312_o.jpg?_nc_cat=106&_nc_sid=84a396&_nc_eui2=AeGJQNP9W7eKOxd27lrSwlomxYFVydwut2bFgVXJ3C63ZvWaaYmVmF9SpckSzn_xhQQ&_nc_ohc=rZNW3v75LIMAX8XrtOR&_nc_ht=scontent-qro1-1.xx&oh=03f6920c10f08f5ff0b6f1c2755a5fd3&oe=5EC7D2E5",
          "photo":  "https://scontent-qro1-1.xx.fbcdn.net/v/t1.0-9/1947407_10203253965412393_1800977331_n.jpg?_nc_cat=100&_nc_sid=d2e176&_nc_eui2=AeFqKFYxM1UaAZ8Os_mjK04bqXt7zwRCX8epe3vPBEJfx3HkTSBHOrnNlWTR0tzUWdo&_nc_ohc=G60Yb2FAC5cAX_AZHfZ&_nc_ht=scontent-qro1-1.xx&oh=9a1e9ce90008b2a8006348df9fdfc6eb&oe=5EC5581E",
          "like": false,
          "bookmark": false,
          "postComment": "Un hueso para la dieta",
          "comments": []
        },
        {
          "username": "pelusi_official",
          "location": "Ciudad de México, México",
          "avatar": "https://scontent-qro1-1.xx.fbcdn.net/v/t1.0-9/44379866_10217113262846167_1434682057987981312_o.jpg?_nc_cat=106&_nc_sid=84a396&_nc_eui2=AeGJQNP9W7eKOxd27lrSwlomxYFVydwut2bFgVXJ3C63ZvWaaYmVmF9SpckSzn_xhQQ&_nc_ohc=rZNW3v75LIMAX8XrtOR&_nc_ht=scontent-qro1-1.xx&oh=03f6920c10f08f5ff0b6f1c2755a5fd3&oe=5EC7D2E5",
          "photo":  "https://scontent-qro1-1.xx.fbcdn.net/v/t1.0-9/1947407_10203253965412393_1800977331_n.jpg?_nc_cat=100&_nc_sid=d2e176&_nc_eui2=AeFqKFYxM1UaAZ8Os_mjK04bqXt7zwRCX8epe3vPBEJfx3HkTSBHOrnNlWTR0tzUWdo&_nc_ohc=G60Yb2FAC5cAX_AZHfZ&_nc_ht=scontent-qro1-1.xx&oh=9a1e9ce90008b2a8006348df9fdfc6eb&oe=5EC5581E",
          "like": false,
          "bookmark": false,
          "postComment": "Siendo un sultan",
          "comments": []
        },
        {
          "username": "pelusi_official",
          "location": "Ciudad de México, México",
          "avatar": "https://scontent-qro1-1.xx.fbcdn.net/v/t1.0-9/44379866_10217113262846167_1434682057987981312_o.jpg?_nc_cat=106&_nc_sid=84a396&_nc_eui2=AeGJQNP9W7eKOxd27lrSwlomxYFVydwut2bFgVXJ3C63ZvWaaYmVmF9SpckSzn_xhQQ&_nc_ohc=rZNW3v75LIMAX8XrtOR&_nc_ht=scontent-qro1-1.xx&oh=03f6920c10f08f5ff0b6f1c2755a5fd3&oe=5EC7D2E5",
          "photo":  "https://scontent-qro1-1.xx.fbcdn.net/v/t1.0-9/1947407_10203253965412393_1800977331_n.jpg?_nc_cat=100&_nc_sid=d2e176&_nc_eui2=AeFqKFYxM1UaAZ8Os_mjK04bqXt7zwRCX8epe3vPBEJfx3HkTSBHOrnNlWTR0tzUWdo&_nc_ohc=G60Yb2FAC5cAX_AZHfZ&_nc_ht=scontent-qro1-1.xx&oh=9a1e9ce90008b2a8006348df9fdfc6eb&oe=5EC5581E",
          "like": false,
          "bookmark": false,
          "postComment": "Siendo un sultan",
          "comments": []
        },
        {
          "username": "pelusi_official",
          "location": "Ciudad de México, México",
          "avatar": "https://scontent-qro1-1.xx.fbcdn.net/v/t1.0-9/44379866_10217113262846167_1434682057987981312_o.jpg?_nc_cat=106&_nc_sid=84a396&_nc_eui2=AeGJQNP9W7eKOxd27lrSwlomxYFVydwut2bFgVXJ3C63ZvWaaYmVmF9SpckSzn_xhQQ&_nc_ohc=rZNW3v75LIMAX8XrtOR&_nc_ht=scontent-qro1-1.xx&oh=03f6920c10f08f5ff0b6f1c2755a5fd3&oe=5EC7D2E5",
          "photo":  "https://scontent-qro1-1.xx.fbcdn.net/v/t1.0-9/1947407_10203253965412393_1800977331_n.jpg?_nc_cat=100&_nc_sid=d2e176&_nc_eui2=AeFqKFYxM1UaAZ8Os_mjK04bqXt7zwRCX8epe3vPBEJfx3HkTSBHOrnNlWTR0tzUWdo&_nc_ohc=G60Yb2FAC5cAX_AZHfZ&_nc_ht=scontent-qro1-1.xx&oh=9a1e9ce90008b2a8006348df9fdfc6eb&oe=5EC5581E",
          "like": false,
          "bookmark": false,
          "postComment": "A dormir",
          "comments": []
        },
        {
          "username": "pelusi_official",
          "location": "Ciudad de México, México",
          "avatar": "https://scontent-qro1-1.xx.fbcdn.net/v/t1.0-9/44379866_10217113262846167_1434682057987981312_o.jpg?_nc_cat=106&_nc_sid=84a396&_nc_eui2=AeGJQNP9W7eKOxd27lrSwlomxYFVydwut2bFgVXJ3C63ZvWaaYmVmF9SpckSzn_xhQQ&_nc_ohc=rZNW3v75LIMAX8XrtOR&_nc_ht=scontent-qro1-1.xx&oh=03f6920c10f08f5ff0b6f1c2755a5fd3&oe=5EC7D2E5",
          "photo":  "https://scontent-qro1-1.xx.fbcdn.net/v/t1.0-9/1947407_10203253965412393_1800977331_n.jpg?_nc_cat=100&_nc_sid=d2e176&_nc_eui2=AeFqKFYxM1UaAZ8Os_mjK04bqXt7zwRCX8epe3vPBEJfx3HkTSBHOrnNlWTR0tzUWdo&_nc_ohc=G60Yb2FAC5cAX_AZHfZ&_nc_ht=scontent-qro1-1.xx&oh=9a1e9ce90008b2a8006348df9fdfc6eb&oe=5EC5581E",
          "like": false,
          "bookmark": false,
          "postComment": "Siendo un sultan",
          "comments": []
        },
        {
          "username": "pelusi_official",
          "location": "Ciudad de México, México",
          "avatar": "https://scontent-qro1-1.xx.fbcdn.net/v/t1.0-9/44379866_10217113262846167_1434682057987981312_o.jpg?_nc_cat=106&_nc_sid=84a396&_nc_eui2=AeGJQNP9W7eKOxd27lrSwlomxYFVydwut2bFgVXJ3C63ZvWaaYmVmF9SpckSzn_xhQQ&_nc_ohc=rZNW3v75LIMAX8XrtOR&_nc_ht=scontent-qro1-1.xx&oh=03f6920c10f08f5ff0b6f1c2755a5fd3&oe=5EC7D2E5",
          "photo":  "https://scontent-qro1-1.xx.fbcdn.net/v/t1.0-9/1947407_10203253965412393_1800977331_n.jpg?_nc_cat=100&_nc_sid=d2e176&_nc_eui2=AeFqKFYxM1UaAZ8Os_mjK04bqXt7zwRCX8epe3vPBEJfx3HkTSBHOrnNlWTR0tzUWdo&_nc_ohc=G60Yb2FAC5cAX_AZHfZ&_nc_ht=scontent-qro1-1.xx&oh=9a1e9ce90008b2a8006348df9fdfc6eb&oe=5EC5581E",
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

<style>
    @import url('https://fonts.googleapis.com/css?family=Lato:300,400&display=swap');
    @import url('https://fonts.googleapis.com/css?family=Pacifico&display=swap');

    :global(body) {
        background: #fafafa;
        color: rgba(38, 38, 38, 0.7);
        font-family: "Lato", sans-serif;
        margin: 0;
        padding: 0;
    }

    :global(h1,h2,h3) {
        margin: 0;
        padding: 0;
    }
</style>

<Header/>
<Main>
    <TimeLine posts={data.posts} />
    <Sidebar {...data.user} />
</Main>
