<template>
  <div>
    <div class="dashboard-container">
      <div class="dashboard-text">项目背景</div>
      <el-row>
        <el-card class="box-card">
          <p class="mytext">网络体系结构中传输层（transport）层的任务是考虑从主机到主机的分组传递服务转向进程到进程的通信信道的问题。由于它支持在终端节点上运行的应用程序之间的通信，因此
            传输层协议有时也称为端到端（end-to-end）协议。两种因素促成了端到端协议的形成。从其上层看，需要使用传输层服务的应用层进程有一些特定的需求。从其下层看，传输层协议赖以运行的下层网络所能提供的服务能力有某些
            限制。因此，问题的关键是设计出各种算法，把下层网络低于要求的特性转变为应用程序所需的高级服务。不同的传输层协议应用这些算法的不同组合。</p>
          <p class="mytext">实验目的：了解应用层协议与传输层协议的关系；掌握 TCP 连接的建立和释放过程以及其重传机制；掌握 TCP 数据传输中编号与确认的过程；理解 FTP 协议的工作原理和常用命令。</p>
        </el-card>
      </el-row>
    </div>
    <div class="dashboard-container">
      <div class="dashboard-text">成员介绍</div>
      <div>
        <el-row gutter="10">
          <el-col :span="4">
            <el-card :body-style="{ padding: '8px' }">
              <img src="https://shadow.elemecdn.com/app/element/hamburger.9cf7b091-55e9-11e9-a976-7f4d0b07eef6.png" class="image">
              <div style="padding: 14px;">
                <p class="headtext">憨憨</p>
                <p class="mytext">大家好，我是组长憨憨，在本次实验中负责完成TCP连接超时重传的任务，说明四次挥手的原理。通过本次实验，我对于TCP连接的原理有了更清晰的理解，学习到了TCP连接机制的合理性，收获良多。</p>
              </div>
            </el-card>
          </el-col>
          <el-col :span="4">
            <el-card :body-style="{ padding: '8px' }">
              <img src="https://shadow.elemecdn.com/app/element/hamburger.9cf7b091-55e9-11e9-a976-7f4d0b07eef6.png" class="image">
              <div style="padding: 14px;">
                <p class="headtext">憨憨</p>
                <p class="mytext">大家好，我是组员憨憨，本次实验中负责报文分析。通过本次实验，对TCP的报文格式有了更清晰的了解。</p>
              </div>
            </el-card>
          </el-col>
          <el-col :span="4">
            <el-card :body-style="{ padding: '8px' }">
              <img src="https://shadow.elemecdn.com/app/element/hamburger.9cf7b091-55e9-11e9-a976-7f4d0b07eef6.png" class="image">
              <div style="padding: 14px;">
                <p class="headtext">憨憨</p>
                <p class="mytext">大家好，我是组员憨憨，在本次TCP实验中，我主要负责完成TCP三次握手以及超时重传的任务，说明三次握手的原理。通过选修计算机网络实验过程，我对计算机网络的相关协议等理论知识理解得更加深刻，让我受益匪浅。</p>
              </div>
            </el-card>
          </el-col>
          <el-col :span="4">
            <el-card :body-style="{ padding: '8px' }">
              <img src="https://shadow.elemecdn.com/app/element/hamburger.9cf7b091-55e9-11e9-a976-7f4d0b07eef6.png" class="image">
              <div style="padding: 14px;">
                <p class="headtext">憨憨</p>
                <p class="mytext">大家好，我是组员憨憨，在本次实验中负责的工作是作为server端，完成三次握手和四次挥手的演示并分析相应报文。本次实验使我对于TCP和FTP等原理有了更清晰的理解，也提高了自己的纠错能力和团队协作能力。</p>
              </div>
            </el-card>
          </el-col>
          <el-col :span="4">
            <el-card :body-style="{ padding: '8px' }">
              <img src="https://shadow.elemecdn.com/app/element/hamburger.9cf7b091-55e9-11e9-a976-7f4d0b07eef6.png" class="image">
              <div style="padding: 14px;">
                <p class="headtext">憨憨</p>
                <p class="mytext">大家好，我是组员憨憨。我在本次TCP实验中负责的工作是报文分析。通过分析报文，我对TCP的工作流程有了更详细的了解，进而更好地理解了TCP的工作原理。</p>
              </div>
            </el-card>
          </el-col>
          <el-col :span="4">
            <el-card :body-style="{ padding: '8px' }">
              <img src="https://shadow.elemecdn.com/app/element/hamburger.9cf7b091-55e9-11e9-a976-7f4d0b07eef6.png" class="image">
              <div style="padding: 14px;">
                <p class="headtext">憨憨</p>
                <p class="mytext">大家好，我是组员憨憨。我在本次TCP实验中负责的工作是建立FTP服务器，维护服务器并且从服务器视角给出分析。以此对TCP双端连接有了更深的理解。</p>
              </div>
            </el-card>
          </el-col>

        </el-row>
      </div>
    </div>
    <div class="dashboard-container">
      <div class="dashboard-text">视频演示</div>
      <div class="demo">
        <video-player ref="videoPlayer" class="video-player vjs-custom-skin" :playsinline="true" :options="playerOptions" />
      </div>
      </el-row>
    </div>

  </div>

</template>
<script>
export default {
  data() {
    return {
      playerOptions: {
        // 播放速度
        playbackRates: [0.5, 1.0, 1.5, 2.0],
        // 如果true,浏览器准备好时开始回放。
        autoplay: false,
        // 默认情况下将会消除任何音频。
        muted: false,
        // 导致视频一结束就重新开始。
        loop: false,
        // 建议浏览器在<video>加载元素后是否应该开始下载视频数据。auto浏览器选择最佳行为,立即开始加载视频（如果浏览器支持）
        preload: 'auto',
        language: 'zh-CN',
        // 将播放器置于流畅模式，并在计算播放器的动态大小时使用该值。值应该代表一个比例 - 用冒号分隔的两个数字（例如"16:9"或"4:3"）
        aspectRatio: '16:9',
        // 当true时，Video.js player将拥有流体大小。换句话说，它将按比例缩放以适应其容器。
        fluid: true,
        sources: [{
          // 类型
          type: 'video/mp4',
          // url地址
          src: require('@/FIFAvideo.mp4') // 本地文件路径要加上require()
        }],
        // 你的封面地址
        poster: 'http://img.cuper.top/GOAT.jpg',
        // 允许覆盖Video.js无法播放媒体源时显示的默认信息。
        notSupportedMessage: '此视频暂无法播放，请稍后再试',
        controlBar: {
          timeDivider: true,
          durationDisplay: true,
          remainingTimeDisplay: false,
          // 全屏按钮
          fullscreenToggle: true
        }
      }

    }
  }
}
</script>
<style lang="scss" scoped>
	.dashboard {
		&-container {
			margin: 30px;
		}

		&-text {
			font-size: 30px;
			line-height: 46px;
		}
	}

	.el-row {
		margin-right: 30px;
		margin-top: 20px;
	}

	.el-col {
		border-radius: 4px;
	}

	.image {
		width: 100%;
	}

	.mytext {
		font-size: 16px;
		word-wrap: break-word;
	}

	.headtext {
		font-size: 20px;
		font-weight: bolder;
	}

	.box-card {
		display: inline-block;
		height: auto;
		float: left;
		width: 100%;
	}

	.demo {
		display: inline-block;
		width: 85%;
		height: 85%;
		line-height: 100px;
		border-radius: 5px;
		overflow: hidden;
		background: #fff;
		position: relative;
		box-shadow: 3px 3px 3px rgba(90, 90, 90, 51);
		margin-top: 20px;
	}

	.demo:hover {
		display: block;
	}
</style>
