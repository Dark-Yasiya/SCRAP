<p align="center">
  <a href="" rel="noopener">
    <img width=100px height=100px src="https://i.ibb.co/JF7Pr3fH/dy-scrap.webp" alt="Scrap">
  </a>
</p>

<h2 align="center">Download Scrap</h2>

<div align="center">

[![Status](https://img.shields.io/badge/status-active-success.svg)]()
[![GitHub Issues](https://img.shields.io/github/issues/Dark-Yasiya/SCRAP.svg)](https://github.com/Dark-Yasiya/SCRAP/issues)
[![GitHub Pull Requests](https://img.shields.io/github/issues-pr/Dark-Yasiya/SCRAP.svg)](https://github.com/Dark-Yasiya/SCRAP/pulls)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](/LICENSE)

</div>

---

<p align="center">The unofficial Scrap API for extracting media from YouTube, Facebook, TikTok, Twitter, and Instagram.
    <br>
</p>

## 📝 Table of Contents

- [About](#about)
- [Getting Started](#getting_started)
- [Usage](#usage)
- [Contributing](../CONTRIBUTING.md)
- [Authors](#authors)

## 🧐 About <a name = "about"></a>

Scrap is an unofficial tool to extract media from various social platforms including YouTube, Facebook, TikTok, Twitter, and Instagram.

## 🚀 Getting Started <a name = "getting_started"></a>

Follow these instructions to install and use Scrap on your local machine for development and testing purposes.

### 📦 Installation

Using **yarn**:
```sh
yarn add @dark-yasiya/scrap
```

Using **npm**:
```sh
npm i @dark-yasiya/scrap
```

## 🎈 Usage <a name="usage"></a>

### Importing the module

```ts
const DY_SCRAP = require('@dark-yasiya/scrap');
const dy_scrap = new DY_SCRAP();
```

### 🔎 Search YouTube Videos

```ts
let query = "Nubawa Soya"; // Replace with a Search query
const data = await dy_scrap.ytsearch(query);
console.log(data);
```

#### Example Response:
```ts
{
  status: true,
  creator: '@Dark-Yasiya',
  results: [
    {
      type: 'video',
      videoId: 'kcw4DJKJZnc',
      url: 'https://youtube.com/watch?v=kcw4DJKJZnc',
      title: 'DILU Beats - Numbawa Soya (හිරිමල් වැස්සේ තෙමිලා) Official Music Video',
      description: 'DILU Beats - Numbawa Soya (හිරිමල් වැස්සේ තෙමිලා) Official Music Video Stream & Download: ...',
      image: 'https://i.ytimg.com/vi/kcw4DJKJZnc/hq720.jpg',
      thumbnail: 'https://i.ytimg.com/vi/kcw4DJKJZnc/hq720.jpg',
      seconds: 293,
      timestamp: '4:53',
      duration: [Object],
      ago: '1 month ago',
      views: 2369854,
      author: [Object]
    },
    {
      type: 'video',
      videoId: 'Xq1m-FxzgVU',
      url: 'https://youtube.com/watch?v=Xq1m-FxzgVU',
      title: 'Nubawa Soya (නුඹව සොයා) - Slow + Reverb  @supunzstudio',
      description: 'About :- Feel the deep emotions of **"Nubawa Soya" (නුඹව සොයා) - Slow + Reverb** by @dilubeats. ✨ This soulful Sri ...',
      image: 'https://i.ytimg.com/vi/Xq1m-FxzgVU/hq720.jpg',
      thumbnail: 'https://i.ytimg.com/vi/Xq1m-FxzgVU/hq720.jpg',
      seconds: 295,
      timestamp: '4:55',
      duration: [Object],
      ago: '1 month ago',
      views: 4607,
      author: [Object]
    },
    {
      type: 'video',
      videoId: '9QzUgVdkLvk',
      url: 'https://youtube.com/watch?v=9QzUgVdkLvk',
      title: 'Nubawa soya Lyrics | නුබව සොයා | krizz | dilu beats',
      description: 'Nubawa soya Lyrics | නුබව සොයා | krizz | dilu beats Original song artist - @DILUBeats Lyrics video - @KRIZZ-28.',
      image: 'https://i.ytimg.com/vi/9QzUgVdkLvk/hq720.jpg',
      thumbnail: 'https://i.ytimg.com/vi/9QzUgVdkLvk/hq720.jpg',
      seconds: 263,
      timestamp: '4:23',
      duration: [Object],
      ago: '1 month ago',
      views: 17745,
      author: [Object]
    },
     ...
  ]
}
```

### 🎵 Download YouTube MP3 (Audio)

```ts
let yt_url = "https://youtube.com/watch?v=AFqtArWpv-w"; // Replace with a YouTube URL
const data = await dy_scrap.ytmp3(yt_url);
console.log(data);
```

#### Example Response:
```ts
{
  status: true,
  creator: '@Dark-Yasiya',
  task_id: '96e4205c-b419-4fcb-ac2d-2ae5b0c0c073',
  result: {
    data: {
      type: 'video',
      videoId: 'AFqtArWpv-w',
      url: 'https://youtube.com/watch?v=AFqtArWpv-w',
      title: 'Nilan Hettiarachchi - ලෙලෙනා | Lelena (Lyrics)',
      description: 'Title | Lelena Artiste | Nilan Hettiarachchi Music Produced by Chamath Sangeeth Lyrics | Dulan ARX ( Dulanja Alwis) Directed by ...',
      image: 'https://i.ytimg.com/vi/AFqtArWpv-w/hq720.jpg',
      thumbnail: 'https://i.ytimg.com/vi/AFqtArWpv-w/hq720.jpg',
      seconds: 194,
      timestamp: '3:14',
      duration: { toString: [Function: toString], seconds: 194, timestamp: '3:14' },
      ago: '3 years ago',
      views: 543179,
      author: { name: 'SL Lyrics', url: 'https://youtube.com/@sllyrics1123' }
    },
    download: {
      url: 'https://storage.devcraftlabs.pro/ytdlp/13-03-2025/nilan-hettiarachchi--96znAfAYL6_www.grabtheclip.com.mp3?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=cU7pKk5PHgIu7CM7Hica%2F20250313%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250313T124621Z&X-Amz-Expires=604800&X-Amz-SignedHeaders=host&X-Amz-Signature=c46c80d998f851aabd9ea3196e6ecb60428dd6d11dd6bfbe5f2ac93d1efa7fa1'
    }
  }
}
```

### 🎥 Download YouTube MP4 (Video)

```ts
let yt_url = "https://youtube.com/watch?v=AFqtArWpv-w"; // Replace with a YouTube URL
let quality = 360; // Choose quality (360, 720, 1080)
const data = await dy_scrap.ytmp4(yt_url, quality);
console.log(data);
```

#### Example Response:
```ts
{
  status: true,
  creator: '@Dark-Yasiya',
  task_id: '51d88d32-b30e-45e2-bd03-f02f79b13457',
  result: {
    data: {
      type: 'video',
      videoId: 'AFqtArWpv-w',
      url: 'https://youtube.com/watch?v=AFqtArWpv-w',
      title: 'Nilan Hettiarachchi - ලෙලෙනා | Lelena (Lyrics)',
      description: 'Title | Lelena Artiste | Nilan Hettiarachchi Music Produced by Chamath Sangeeth Lyrics | Dulan ARX ( Dulanja Alwis) Directed by ...',
      image: 'https://i.ytimg.com/vi/AFqtArWpv-w/hq720.jpg',
      thumbnail: 'https://i.ytimg.com/vi/AFqtArWpv-w/hq720.jpg',
      seconds: 194,
      timestamp: '3:14',
      duration: { toString: [Function: toString], seconds: 194, timestamp: '3:14' },
      ago: '3 years ago',
      views: 543207,
      author: { name: 'SL Lyrics', url: 'https://youtube.com/@sllyrics1123' }
    },
    download: {
      url: 'https://storage.devcraftlabs.pro/ytdlp/13-03-2025/nilan-hettiarachchi--To59nEVBKP_www.grabtheclip.com.mp4?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=cU7pKk5PHgIu7CM7Hica%2F20250313%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250313T130726Z&X-Amz-Expires=604800&X-Amz-SignedHeaders=host&X-Amz-Signature=8bf8c1963c333e568e53a38ce8af0c09f1f22775a3b78d3ee800f315bf4664f7'
    }
  }
}
```

### 🎵 Download YouTube MP3 V2 (Audio)

```ts
let yt_url = "https://youtube.com/watch?v=AFqtArWpv-w"; // Replace with a YouTube URL
const data = await dy_scrap.ytmp3_v2(yt_url);
console.log(data);
```

#### Example Response:
```ts
{
  status: true,
  creator: '@Dark-Yasiya',
  task_id: 'ECoItzNhgLoh8fEv6QIkqCM',
  result: {
    data: {
      type: 'video',
      videoId: 'AFqtArWpv-w',
      url: 'https://youtube.com/watch?v=AFqtArWpv-w',
      title: 'Nilan Hettiarachchi - ලෙලෙනා | Lelena (Lyrics)',
      description: 'Title | Lelena Artiste | Nilan Hettiarachchi Music Produced by Chamath Sangeeth Lyrics | Dulan ARX ( Dulanja Alwis) Directed by ...',
      image: 'https://i.ytimg.com/vi/AFqtArWpv-w/hq720.jpg',
      thumbnail: 'https://i.ytimg.com/vi/AFqtArWpv-w/hq720.jpg',
      seconds: 194,
      timestamp: '3:14',
      duration: { toString: [Function: toString], seconds: 194, timestamp: '3:14' },
      ago: '3 years ago',
      views: 543179,
      author: { name: 'SL Lyrics', url: 'https://youtube.com/@sllyrics1123' }
    },
    download: {
      url: 'https://pauline27.oceansaver.in/pacific/?ECoItzNhgLoh8fEv6QIkqCM'
    }
  }
}
```

### 🎥 Download YouTube MP4 V2 (Video)

```ts
let yt_url = "https://youtube.com/watch?v=AFqtArWpv-w"; // Replace with a YouTube URL
let quality = 360; // Choose quality (360, 720, 1080)
const data = await dy_scrap.ytmp4_v2(yt_url, quality);
console.log(data);
```

#### Example Response:
```ts
{
  status: true,
  creator: '@Dark-Yasiya',
  task_id: 'GGPFjw8HjBX8XQPQ4Anduop',
  result: {
    data: {
      type: 'video',
      videoId: 'AFqtArWpv-w',
      url: 'https://youtube.com/watch?v=AFqtArWpv-w',
      title: 'Nilan Hettiarachchi - ලෙලෙනා | Lelena (Lyrics)',
      description: 'Title | Lelena Artiste | Nilan Hettiarachchi Music Produced by Chamath Sangeeth Lyrics | Dulan ARX ( Dulanja Alwis) Directed by ...',
      image: 'https://i.ytimg.com/vi/AFqtArWpv-w/hq720.jpg',
      thumbnail: 'https://i.ytimg.com/vi/AFqtArWpv-w/hq720.jpg',
      seconds: 194,
      timestamp: '3:14',
      duration: { toString: [Function: toString], seconds: 194, timestamp: '3:14' },
      ago: '3 years ago',
      views: 543207,
      author: { name: 'SL Lyrics', url: 'https://youtube.com/@sllyrics1123' }
    },
    download: {
      url: 'https://joan48.oceansaver.in/pacific/?GGPFjw8HjBX8XQPQ4Anduop'
    }
  }
}
```

### 🎭 Facebook Downloader

```ts
let fb_url = "https://fb.watch/9WktuN9j-z/"; // Replace with a Facebook URL
const data = await dy_scrap.facebook(fb_url);
console.log(data);
```

#### Example Response:
```ts
{
  success: true,
  code: 200,
  creator: '@Dark-Yasiya',
  result: {
    title: 'No video title',
    desc: 'No video description...',
    duration: '18 seconds',
    image: 'https://scontent-msp1-1.xx.fbcdn.net/v/t15.5256-10/150364106_175310434146963_1171304898769276273_n.jpg?_nc_cat=102&ccb=1-7&_nc_sid=a27664&_nc_ohc=ep8ZhVQoaj0Q7kNvgHTLv70&_nc_zt=23&_nc_ht=scontent-msp1-1.xx&_nc_gid=AaQEduVOoSIjx7qp3UCMwo6&oh=00_AYHihgtA5Vnv04lJr3dsAv9vojGoQah9ZTJ4LC3r1g2hEQ&oe=67D8C978 ',
    sd: 'https://video-msp1-1.xx.fbcdn.net/o1/v/t2/f2/m69/AQPg5tN56yX48TZ2QxjDGBev8O-BhQhyfWJUdMSJK26wGm4i4PE1y3MjsR4zYKD78nX9BuiazVXO8Evr-iG1dtUo.mp4?strext=1&_nc_cat=111&_nc_sid=8bf8fe&_nc_ht=video-msp1-1.xx.fbcdn.net&_nc_ohc=W9OB0bwrRMMQ7kNvgH2chZa&efg=eyJ2ZW5jb2RlX3RhZyI6Inhwdl9wcm9ncmVzc2l2ZS5GQUNFQk9PSy4uQzMuNDI2LnN2ZV9zZCIsInhwdl9hc3NldF9pZCI6Mjk0OTgzNzIzMzM2OTY2LCJhc3NldF9hZ2VfZGF5cyI6MTQ3NywidmlfdXNlY2FzZV9pZCI6MTAxMjIsImR1cmF0aW9uX3MiOjE4LCJ1cmxnZW5fc291cmNlIjoid3d3In0%3D&ccb=17-1&_nc_zt=28&oh=00_AYFK4h8ZjSyWNjQOWGlFCtAWnNhsbtva00XEJEf7sj1R1g&oe=67D89D8F&dl=1',
    hd: 'https://video-msp1-1.xx.fbcdn.net/o1/v/t2/f2/m69/AQMEqP8Bn5r2OLm2eYG34GaN2mPScWj3J7wLC5h8PWK8txJcozcAmXnh8XcZjtAhhlGNYZcWXTgnxWJhMtBlzjEZ.mp4?strext=1&_nc_cat=101&_nc_sid=5e9851&_nc_ht=video-msp1-1.xx.fbcdn.net&_nc_ohc=NTofgOUfrmAQ7kNvgG7Hjam&efg=eyJ2ZW5jb2RlX3RhZyI6Inhwdl9wcm9ncmVzc2l2ZS5GQUNFQk9PSy4uQzMuOTYwLmRhc2hfaDI2NC1iYXNpYy1nZW4yXzcyMHAiLCJ4cHZfYXNzZXRfaWQiOjI5NDk4MzcyMzMzNjk2NiwiYXNzZXRfYWdlX2RheXMiOjE0NzcsInZpX3VzZWNhc2VfaWQiOjEwMTIyLCJkdXJhdGlvbl9zIjoxOCwidXJsZ2VuX3NvdXJjZSI6Ind3dyJ9&ccb=17-1&vs=e2f19357eb88c03c&_nc_vs=HBksFQIYOnBhc3N0aHJvdWdoX2V2ZXJzdG9yZS9HQjYyTGh3VE5uYll4eEVDQUp0ZVRqZWtiLThiYm1kakFBQUYVAALIAQAVAhg6cGFzc3Rocm91Z2hfZXZlcnN0b3JlL0dDbzJId2txSnhhZHdONEFBUGp2cWRDVzNtSUxidjRHQUFBRhUCAsgBACgAGAAbAogHdXNlX29pbAExEnByb2dyZXNzaXZlX3JlY2lwZQExFQAAJoyU2oCokoYBFQIoAkMzLBdAMhmZmZmZmhgZZGFzaF9oMjY0LWJhc2ljLWdlbjJfNzIwcBEAdQIA&_nc_zt=28&oh=00_AYEORFAEbMT6lCP-LLnLGhH5w3xDRGXHPNyLrfFGH3cpHg&oe=67D89679&dl=1'
  }
}
```

### 📥 TikTok Downloader

```ts
let tt_url = "https://vt.tiktok.com/ZSje1Vkup/"; // Replace with a TikTok URL
const data = await dy_scrap.tiktok(tt_url);
console.log(data);
```

#### Example Response:
```ts
{
  status: true,
  creator: '@Dark-Yasiya',
  result: {
    id: '7263749907935284485',
    region: 'ID',
    title: 'weem segede gaban #fyp #Monca ',
    cover: 'https://tikwm.com/video/cover/7263749907935284485.webp',
    duration: 37,
    play: 'https://tikwm.com/video/media/play/7263749907935284485.mp4',
    sd: 'https://tikwm.com/video/media/wmplay/7263749907935284485.mp4',
    hd: 'https://tikwm.com/video/media/hdplay/7263749907935284485.mp4',
    music: 'https://tikwm.com/video/music/7263749907935284485.mp3',
    play_count: 38379,
    digg_count: 1920,
    comment_count: 47,
    share_count: 126,
    download_count: 365,
    collect_count: 609
  }
}
```

### 🐦 Twitter Downloader

```ts
let tw_url = "https://twitter.com/futurism/status/882987478541533189"; // Replace with a Twitter URL
const data = await dy_scrap.twitter(tw_url);
console.log(data);
```

#### Example Response:
```ts
{
  success: true,
  creator: '@Dark-Yasiya',
  result: {
    desc: 'These tires can even climb stairs https://t.co/ymr4KK15oI',
    thumb: 'https://pbs.twimg.com/amplify_video_thumb/882986340605939712/img/k-NlEfo7z0Xvo9ab.jpg',
    video_sd: 'https://twdown.net/https://video.twimg.com/amplify_video/882986340605939712/vid/480x480/XcNdeyAihVz48yfL.mp4',
    video_hd: 'https://twdown.net/https://video.twimg.com/amplify_video/882986340605939712/vid/720x720/1Vn9i-z2JFABEmiN.mp4',
    audio: 'https://twdown.net/https://video.twimg.com/amplify_video/882986340605939712/vid/240x240/h9r1X049XDiYEHlP.mp4'
  }
}
```

### 🎨 Instagram Downloader

```ts
let ig_url = "https://www.instagram.com/justmike/reel/DHH74SBA4So/"; // Replace with a Instagram URL
const data = await dy_scrap.instagram(ig_url);
console.log(data);
```

#### Example Response:
```ts
{
  success: true,
  creator: '@Dark-Yasiya',
  result: {
    thumbnail: 'https://scontent-yyz1-1.cdninstagram.com/v/t51.2885-15/484170083_18500130616006959_2257466502496613651_n.jpg?stp=dst-jpg_e35_p1080x1080_sh0.08_tt6&_nc_ht=scontent-yyz1-1.cdninstagram.com&_nc_cat=103&_nc_oc=Q6cZ2AGcB2HrYihrI_CITl_w-MLbq5WY_ic_-Gj4bmTezHxETyo6c7sZEGWMb2eQnworYWs&_nc_ohc=u646ctEcErgQ7kNvgH2OWOg&_nc_gid=1f1c7e5a54104c908cdf2ef096379b40&edm=ANTKIIoBAAAA&ccb=7-5&oh=00_AYFlZjhUYS5zg_wReFqdVEqN4hOt_wwTww3DBm-ZPZ_Eig&oe=67D8C789&_nc_sid=d885a2',
    video: 'https://scontent-yyz1-1.cdninstagram.com/o1/v/t16/f2/m86/AQMUgDU9uSHrAmQh9fSNlHG-a767PKfKX4ZLqWN6jaWigswdlDOdtTq5tsJtqvcpi8h0FuMFpvkh7nd7I-fuERGHN-v-Q8UFUKLhblY.mp4?stp=dst-mp4&efg=eyJxZV9ncm91cHMiOiJbXCJpZ193ZWJfZGVsaXZlcnlfdnRzX290ZlwiXSIsInZlbmNvZGVfdGFnIjoidnRzX3ZvZF91cmxnZW4uY2xpcHMuYzIuNzIwLmJhc2VsaW5lIn0&_nc_cat=109&vs=1199009181659430_2422786755&_nc_vs=HBksFQIYUmlnX3hwdl9yZWVsc19wZXJtYW5lbnRfc3JfcHJvZC9GMDRBNDIzMEIzRTA4RkUxNjdBREJEMjg0NEVGODVCOF92aWRlb19kYXNoaW5pdC5tcDQVAALIAQAVAhg6cGFzc3Rocm91Z2hfZXZlcnN0b3JlL0dKbHR6eHlfWEpDQTNKb0RBSXR4NWhTbHZlUkRicV9FQUFBRhUCAsgBACgAGAAbABUAACaAzJ2BiO6aQBUCKAJDMywXQDrcKPXCj1wYEmRhc2hfYmFzZWxpbmVfMV92MREAdf4HAA%3D%3D&_nc_rid=1f1c7102c1&ccb=9-4&oh=00_AYF20H9kdvUV9Mr6WnuNtIvLQ1JZN4zDSTKE3-013E6jeA&oe=67D4B1E5&_nc_sid=d885a2'
  }
}
```

## ✍️ Authors <a name = "authors"></a>

- **[@Dark-Yasiya](https://github.com/Dark-Yasiya)** - Creator & Maintainer

See the list of [contributors](https://github.com/Dark-Yasiya/SCRAP/contributors) who participated in this project.

