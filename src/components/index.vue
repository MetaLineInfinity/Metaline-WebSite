<template>
  <div class="index-content" @click="is_show = false">
    <div>
      <div id="header" class="section1-header">
        <img class="section1-img2" src="https://d3vndanhiwhas.cloudfront.net/static/img/common/logo.png?v=1.1.3" alt="">
        <div class="blind-box" @click="footerClick('https://nft.metaline.games')">
          <img src="https://d3vndanhiwhas.cloudfront.net/static/img/common/ico_boxblue.png" alt="">
          <p>Mystery Box</p>
        </div>
      </div>
      <div id="home" class="header">
        <p class="header-title">Community & How to Play</p>
        <p class="header-content-1">A web3 multiplayer sailing game under development</p>
        <p class="header-content-2">Join the chamber of commerce, manufacture Goods, pve, play with friends, jump in the metaverse, create a great era of navigation that belongs to you alone!</p>
      </div>
      <div class="section1">
        <img src="https://d3vndanhiwhas.cloudfront.net/static/img/common/smoke.gif?v=1.1.3" alt="" class="smoke">
        <img class="girlwhites" src="https://d3vndanhiwhas.cloudfront.net/static/img/common/girlwhites.gif?v=1.1.3" alt="">
        <img class="beermans" src="https://d3vndanhiwhas.cloudfront.net/static/img/common/beermans.gif?v=1.1.3" alt="">
        <img class="hatgirl" src="https://d3vndanhiwhas.cloudfront.net/static/img/common/hatgirl.gif?v=1.1.3" alt="">
        <img class="boys" src="https://d3vndanhiwhas.cloudfront.net/static/img/common/boys.gif?v=1.1.3" alt="">
        <img class="axman" src="https://d3vndanhiwhas.cloudfront.net/static/img/common/axman.gif?v=1.1.3" alt="">
        <img draggable="false" class="section1-line" src="https://d3vndanhiwhas.cloudfront.net/static/img/common/line01.png?v=1.1.3" alt="">
      </div>
      <div class="section-2">
        <div class="video" data-aos="zoom-in" data-aos-delay="200">
          <div class="video-bg">
            <div class="video-corner">
              <div class="corner1"></div>
              <div class="corner2"></div>
              <div class="corner3"></div>
              <div class="corner4"></div>
            </div>
            <div class="video-content">
              <img v-if="!show_video" @click="playVideo" draggable="false" src="https://d3vndanhiwhas.cloudfront.net/m/img/img_play.png" alt="">
              <video v-else ref="video" class="iframeCss" controls poster="https://d3vndanhiwhas.cloudfront.net/static/img/common/videobg.png?v=1.1.3">
                <source src="https://d3vndanhiwhas.cloudfront.net/video/metaline.mp4" type="video/mp4">
              </video>
            </div>
          </div>
          <img draggable="false" class="section2-5-line" src="https://d3vndanhiwhas.cloudfront.net/static/img/common/line04.png?v=1.1.3" alt="">
        </div>

        <div class="section2-1" id="play-to-own" data-aos="zoom-in" data-aos-delay="250">
          <div class="section2-1-top">
            <img class="section2-1-ship" src="https://d3vndanhiwhas.cloudfront.net/m/img/img_boat03.png" alt="">
            <div class="section2-2-middle">
              <p class="section2-1-top-title">Play To Own</p>
              <p class="section2-1-top-content">More than 1,000 different goods, characters, and ships are on the Blockchain. own, manufacture, take risks, and buy what you want</p>
              <div class="section2-1-imgs">
                <img src="https://d3vndanhiwhas.cloudfront.net/static/img/common/icomini_arena.png?v=1.1.3" alt="">
                <img src="https://d3vndanhiwhas.cloudfront.net/static/img/common/icomini_production.png?v=1.1.3" alt="">
                <img src="https://d3vndanhiwhas.cloudfront.net/static/img/common/icomini_quest.png?v=1.1.3" alt="">
                <img src="https://d3vndanhiwhas.cloudfront.net/static/img/common/icomini_mission.png?v=1.1.3" alt="">
                <img src="https://d3vndanhiwhas.cloudfront.net/static/img/common/icomini_battle.png?v=1.1.3" alt="">
              </div>
            </div>
          </div>
          <div class="section2-1-bottom">
            <div draggable="false" class="open-sea"><a @click="footerClick('https://opensea.io/collection/metaline-mysterybox')">OpenSea</a></div>
            <div draggable="false" class="uniswap"><a @click="footerClick('https://uniswap.org/')">UniSwap</a></div>
          </div>
          <img draggable="false" class="section2-1-line" src="https://d3vndanhiwhas.cloudfront.net/static/img/common/line02.png?v=1.1.3" alt="">
        </div>
        <div class="section2-2" id="hero" data-aos="fade-up" data-aos-delay="150">
          <img draggable="false" class="section2-2-img-1" src="https://d3vndanhiwhas.cloudfront.net/static/img/common/img_sea02.png?v=1.1.3" alt="">
          <img data-aos="fade-up" data-aos-delay="250" draggable="false" class="section2-2-img-2" src="https://d3vndanhiwhas.cloudfront.net/static/img/common/hero.gif?v=1.1.3" alt="">
          <p class="hero-title">Hero</p>
          <p class="hero-content">Heroes will take you to different ports, shuttle to various games, will you want to be a sailor or a pirate</p>
        </div>
        <div class="section2-3" data-aos="fade-up" data-aos-delay="150">
          <div class="section2-3-title">
            <p>Private Ship</p>
            <p>The ferryman that appears in the game, do you want to become the captain? first collect materials!</p>
          </div>
          <div class="section-ship">
            <div data-aos="fade-right"
                 data-aos-offset="300"
                 data-aos-delay="100"
                 data-aos-easing="ease-in-sine">
              <img draggable="false" class="ship1" src="https://d3vndanhiwhas.cloudfront.net/static/img/common/img_boat02.gif?v=1.1.3" alt="">
            </div>
            <div data-aos="fade-left"
                 data-aos-offset="300"
                 data-aos-easing="ease-in-sine"
                 data-aos-delay="300">
              <img draggable="false" class="ship2" src="https://d3vndanhiwhas.cloudfront.net/static/img/common/img_boat01.gif?v=1.1.3" alt="">
            </div>
          </div>
          <!--          <img draggable="false" class="section2-3-bottom" src="https://d3vndanhiwhas.cloudfront.net/m/img/section2-3-bottom.png" alt="">-->
          <img draggable="false" class="section2-3-line" src="https://d3vndanhiwhas.cloudfront.net/static/img/common/line03.png?v=1.1.3" alt="">
        </div>
        <div class="section2-4" data-aos="fade-up" data-aos-delay="150" id="map">
          <img draggable="false" class="section2-4-line" src="https://d3vndanhiwhas.cloudfront.net/static/img/common/line03.png?v=1.1.3" alt="">
        </div>
        <div class="section2-5" data-aos="fade-up" data-aos-delay="150" id="building">
          <div class="section2-5-imgs">
            <div data-aos="fade-right"
                 class="section2-5-imgs-top"
                 data-aos-offset="300"
                 data-aos-easing="ease-in-sine">
              <img draggable="false" class="section2-5-imgs-1" src="https://d3vndanhiwhas.cloudfront.net/static/img/common/img_pic01.png?v=1.1.3" alt="">
              <img draggable="false" data-aos="zoom-in" data-aos-delay="500" class="line1" src="https://d3vndanhiwhas.cloudfront.net/static/img/common/lingred.png?v=1.1.3" alt="">
              <div class="section2-5-content section2-5-content1">
                <p>Building</p>
                <p>Create your own house, collect materials on the island, fantastic things will happen here</p>
              </div>
            </div>
            <div data-aos="fade-left"
                 data-aos-offset="300"
                 data-aos-easing="ease-in-sine" class="section2-5-imgs-bottom">
              <div class="section2-5-content section2-5-right">
                <p>Building</p>
                <p>Want to make more money? Produce or loot more coins to exchange here</p>
              </div>
              <img draggable="false" class="section2-5-imgs-2" src="https://d3vndanhiwhas.cloudfront.net/static/img/common/img_pic02.png?v=1.1.3" alt="">
              <img draggable="false" data-aos="zoom-in" data-aos-delay="500" class="line2" src="https://d3vndanhiwhas.cloudfront.net/static/img/common/lingwhite.png?v=1.1.3" alt="">
            </div>
          </div>
          <img draggable="false" data-aos="zoom-in" data-aos-delay="200"  class="section2-5-bottom" src="https://d3vndanhiwhas.cloudfront.net/static/img/common/img_bgbig02.png?v=1.1.3" alt="">
          <img draggable="false"  class="section2-5-line" src="https://d3vndanhiwhas.cloudfront.net/static/img/common/line04.png?v=1.1.3" alt="">
        </div>
      </div>
      <div class="road-map" data-aos="zoom-in" data-aos-delay="250">
        <p>Project RoadMap</p>
        <div class="road-map-content">
          <div class="road-1 road-right-item">
            <p>2023.01</p>
            <p>Complete the initial development and announce the funding news</p>
          </div>
          <div class="road-2 road-left-item">
            <p>2023.02</p>
            <p>Launch the first round of NFT sale on Arbitrum
            </p>
          </div>
          <div class="road-3 road-right-item">
            <p>2023.03</p>
            <p>Launch the official version of the game, mystery box public sale, </p>
          </div>
          <div class="road-4 road-left-item">
            <p>2023.04</p>
            <p>Integrate more in-game ports</p>
          </div>
          <div class="road-5 road-right-item">
            <p>2023.05</p>
            <p>Launch the PVE battle mode and the guild system
            </p>
          </div>
          <div class="road-6 road-left-item">
            <p>2023.06</p>
            <p>List on Google and Apple store</p>
          </div>
          <div class="road-7 road-right-item">
            <p>2023.07</p>
            <p>Metaline 2.0, launch new game season and more game items and characters </p>
          </div>
        </div>
        <img draggable="false" class="section2-3-line" src="https://d3vndanhiwhas.cloudfront.net/static/img/common/line03.png?v=1.1.3" alt="">
      </div>
      <div class="partner">
        <img draggable="false" src="https://d3vndanhiwhas.cloudfront.net/static/img/common/partner-logo.png" alt="">
        <div class="partner-items">
          <div class="partner-item">
            <p>Resource</p>
            <a @click="footerClick('https://whitepaper.metaline.games/')">WhitePaper</a>
            <a @click="footerClick('https://github.com/MetaLineInfinity')">Github</a>
          </div>
          <div class="partner-item">
            <p>Social</p>
            <a @click="footerClick('https://twitter.com/metaline001')">Twitter</a>
            <a @click="footerClick('https://discord.gg/EemEKjNs4M')">Discord</a>
            <a @click="footerClick('https://link.medium.com/n9AZRIAd4vb')">Medium</a>
          </div>
          <div class="partner-item">
            <p>Contact</p>
            <a href="mailto:business@metaline.games">business@metaline.games</a>
          </div>
        </div>
      </div>
      <div class="footer">@2022-2023 MetaLine All Rights Reserved.</div>
    </div>
    <transition>
      <div class="loading-bg" v-if="loading">
        <div class="loading"></div>
      </div>
    </transition>
  </div>
</template>

<style>
.v-enter-active,
.v-leave-active {
  transition: opacity 0.5s ease;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}
</style>

<script>
import 'echarts/lib/component/tooltip'
let ECharts = require('echarts/lib/echarts')
require('echarts/lib/chart/pie')
export default {
  name: 'index',
  data () {
    return {
      show_video: false,
      is_show: false,
      loading: true,
      display: false,
      iframeWidth: '', // 宽度
      iframeHeight: '', // 高度
      materialData: {
        type: '0',
        url: '', // 外部网址链接
        logoUrl: ''
      }
    }
  },
  mounted () {
    this.imgLoading()
    let chart = ECharts.init(document.getElementById('myChart'))
    chart.setOption({
      tooltip: {
        show: true,
        formatter: '{b}:{c}',
        // position: function (p) {
        //   return [p[0] + 35, p[1] - 10]
        // },
        textStyle: {
          fontSize: '15'
        }
      },
      series: [
        {
          type: 'pie',
          radius: [50, 200],
          center: ['50%', '50%'],
          roseType: 'area',
          itemStyle: {
            borderRadius: 8,
            normal: {
              label: {
                show: true,
                formatter: '{b}: {d}%',
                textStyle: {
                  fontSize: '12',
                  fontFamily: 'fzxs',
                  lineHeight: 15
                }
              }
            }
          },
          animation: true,
          data: [
            {value: 66000000, name: 'Token Sale', itemStyle: {color: '#5670C3'}, label: '123'},
            {value: 60000000, name: 'Yield farming', itemStyle: {color: '#97CC79'}},
            {value: 36000000, name: 'Marketing and community Treasury', itemStyle: {color: '#FBDA69'}},
            {value: 75000000, name: 'Ecosystem development', itemStyle: {color: '#F67072'}},
            {value: 45000000, name: 'Team/Advisors/Employees', itemStyle: {color: '#7CBFDC'}},
            {value: 18000000, name: 'Airdrop Treasury', itemStyle: {color: '#51B17E'}}
          ]
        }
      ]
    })
  },
  methods: {
    footerClick (url) {
      this.createSuperLabel(url, url)
    },
    createSuperLabel (url, id) {
      let a = document.createElement('a')
      a.setAttribute('href', url)
      a.setAttribute('target', '_blank')
      a.setAttribute('id', id)
      // 防止反复添加
      if (!document.getElementById(id)) {
        document.body.appendChild(a)
      }
      a.click()
    },
    imgLoading () {
      const _this = this
      let imgList = document.getElementsByTagName('img')// 图片集合
      let imgCount = imgList.length// 图片总数
      let imgLoad = 0// 加载完成的图片数量

      for (let i = 0; i < imgCount; i++) {
        imgList[i].onload = () => {
          imgLoad++
          if (imgLoad === imgCount) {
            setTimeout(function () {
              _this.loading = false
              _this.display = true
            }, 1000)
          }
        }
        setTimeout(() => {
          if (!this.display) {
            this.loading = false
            this.display = !this.display
          }
        }, 5000)
      }
    },
    playVideo () {
      const _this = this
      this.show_video = true
      setTimeout(function () {
        _this.$refs.video.play()
      }, 100)
    }
  }
}
</script>
