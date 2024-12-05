<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>구름 아카이브 :: 구름을 그리는 사람들</title>
    <style>
        @font-face {
    font-family: 'Happiness-Sans'; /* 커스텀 폰트 이름 */
    src: url('./fonts/Happiness-Sans-Regular.ttf') format('truetype');
    font-weight: normal;
    font-style: normal;
}

body, html {
    margin: 0;
    padding: 0;
    height: 100%;
    font-family: 'Happiness-Sans', Arial, sans-serif; /* 커스텀 폰트 우선 적용 */
    line-height: 1.6;
    color: #333;
    scroll-behavior: smooth;
    background: linear-gradient(rgb(197, 199, 221), rgb(0, 78, 146));
    background-repeat: no-repeat;
    background-size: cover;
}
ul {
        list-style-type: none; /* 리스트 점 제거 */
        padding: 0; /* 기본 패딩 제거 */
        margin: 0; /* 기본 마진 제거 */
    }

/* 특정 요소에도 커스텀 폰트 적용 */
h1, p, .navbar a, .footer a {
    font-family: 'Happiness-Sans', Arial, sans-serif;
         }
        /* 눈금자 스타일 */
.progress-bar-ruler {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 10px;
    color: white;
    pointer-events: none; /* 클릭 방지 */
}

.progress-bar-ruler div {
    position: relative;
    transform: translateX(-50%);
}
body, html {
            margin: 0;
            padding: 0;
            height: 100%;
            font-family: 'Happiness-Sans', './fonts/Happiness-Sans-Regular.ttf', sans-serif; /* 2. 커스텀 폰트 적용 */
            line-height: 1.6;
            color: #333;
            scroll-behavior: smooth;
            background: linear-gradient(rgb(197, 199, 221), rgb(0, 78, 146));
            background-repeat: no-repeat;
            background-size: cover;
        }

        .clouds-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 1;
            pointer-events: auto;
            overflow: hidden;
        }
        .footer {
            position: fixed;
            bottom: 0;
            width: 100%;
            background:rgba(132, 189, 246, 0.818);
            padding: 10px 0;
            text-align: center;
            z-index: 1000;
        }

        .footer a {
            color: rgb(255, 255, 255);
            margin: 0 15px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.2em;
            font-family: 'Happiness-Sans', './fonts/Happiness-Sans-Regular.ttf', sans-serif; /* 3. 링크에도 커스텀 폰트 적용 */
        }

        .footer a:hover {
            text-decoration: underline;
        }

        .cloud {
    position: absolute;
    width: 150px; /* 구름 크기 조정 */
    height: 100px; /* 구름 높이 조정 */
    background-size: contain; /* 이미지 크기 조정 */
    background-repeat: no-repeat; /* 이미지 반복 방지 */
    background-position: center; /* 이미지 중앙 정렬 */
    animation: floatClouds linear infinite;
    cursor: pointer;
}
        @keyframes floatClouds {
            from {
                transform: translateX(100vw);
            }
            to {
                transform: translateX(-200vw);
            }
        }
        .image-popup {
        display: none;
        position: fixed;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        background-color: rgba(132, 189, 246, 0.818);
        padding: 20px;
        box-shadow: 0 4px 10px rgba(0, 0, 0, 0.5);
        z-index: 2000;
        border-radius: 10px;
        text-align: center;
        max-width: 90%; /* 팝업 최대 너비를 화면 90%로 제한 */
        max-height: 90%; /* 팝업 최대 높이를 화면 90%로 제한 */
        overflow: auto; /* 이미지가 크면 내부에서 스크롤 가능 */
    }

    .image-popup img {
        max-width: 100%; /* 이미지가 팝업 너비를 넘지 않도록 제한 */
        max-height: 80%; /* 닫기 버튼 공간을 고려해 이미지 높이를 제한 */
        margin-bottom: 10px;
    }

    .image-popup button {
        background-color: rgba(132, 189, 246, 0.818);
        color: white;
        border: none;
        padding: 10px 20px;
        cursor: pointer;
        border-radius: 5px;
    }
        .navbar {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(132, 189, 246, 0.818);
            padding: 10px 0;
            text-align: center;
            z-index: 1000;
        }
        .navbar a {
            color: white;
            margin: 0 15px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.2em;
        }
        .section {
        
            display: flex;
            flex-direction: column;
            justify-content: center; /* 세로 가운데 정렬 */
            align-items: center; /* 가로 가운데 정렬 */
            text-align: center; /* 텍스트 중앙 정렬 */
            padding: 80px 20px; /* 섹션 간격 조정 */
            margin: 0 auto; /* 섹션이 화면 중앙에 위치 */
            max-width: auto; /* 문단의 최대 너비 설정 */
            box-sizing: border-box; /* 패딩 포함 크기 계산 */
            line-height: 1.8; /* 줄 간격 조정 */
            color: white; /* 텍스트 색상 */
            background-size: cover;
            background-attachment: fixed;
            
        }

        h1 {
    font-size: 3em; /* 제목 크기 */
    margin: 20px 0; /* 위아래 간격을 20px로 설정 */
    padding-top: 100px; /* 상단 여백 추가 */
    text-align: justify; /* 제목 가운데 정렬 */
    letter-spacing: -0.02em; /* 글자 간격 조절 */
    word-break: keep-all; /* 단어를 가능한 한 줄 바꿈하지 않음 */
    line-height: 1.2; /* 줄 간격 조정 */
}


p {
    font-size: 3em; /* 제목 크기 */
    margin: 20px 0; /* 위아래 간격을 20px로 설정 */
    padding-top: 100px; /* 상단 여백 추가 */
    text-align: center; /* 제목 가운데 정렬 */
    letter-spacing: -0.02em; /* 글자 간격 조절 */
    word-break: keep-all; /* 단어를 가능한 한 줄 바꿈하지 않음 */
    line-height: 2; /* 줄 간격 조정 */
}
        .high-clouds {
            background-image: url('./images/1.jpg');
        }
        .middle-clouds {
            background-image: url('./images/2.jpg');
        }
        .low-clouds {
            background-image: url('./images/AdobeStock_928181402.jpg');
        }
        .vertical-clouds {
            background-image: url('./images/AdobeStock_885081248.jpg');
  
  
 }
        h1 {
            font-size: 3em;
            margin: 0;
        }
        p {
            max-width: 600px;
            margin: 20px auto;
            font-size: 1.2em;
        }
        /* CSS: 스크롤 진행 상황 바 */
.progress-bar-container {
    position: fixed;
    top: 50px; /* 헤더 바로 밑 */
    left: 0;
    width: 100%;
    height: 10px;
    background: rgba(200, 200, 200, 0.3);
    z-index: 1000;
}
.progress-bar {
    height: 100%;
    width: 0;
    background: #007BFF; /* 진행 바 색상 */
    transition: width 0.1s ease;
}
/* PDF Viewer 스타일 */
#pdfViewerOverlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.8);
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 2000;
    opacity: 0;
    pointer-events: none;
    transition: opacity 1s ease;
}
#pdfViewerOverlay.show {
    opacity: 1;
    pointer-events: auto;
}
#pdfViewerContainer {
    background: white;
    padding: 20px;
    border-radius: 10px;
    text-align: center;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.5);
}
#pdfCanvas {
    width: 100%;
    max-width: 800px;
    height: auto;
}
#closePdfViewer {
    margin-top: 10px;
    padding: 10px 20px;
    background: #007BFF;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}
ul li {
    max-width: 800px; /* 가로 최대 너비 제한 */
    font-size: 16px; /* 본문 크기 */
    margin: 130px 0; /* 본문 간격 */
    text-align: justify; /* 본문 양쪽 정렬 */
    letter-spacing: 0.0em; /* 글자 간격 조정 */
    word-break: keep-all; /* 단어 줄바꿈 방지 */
    line-height: 2; /* 줄 간격 */
    color: white; /* 본문 텍스트 색상 */
    }

    </style>
</head>
<body>
    <div id="pdfOverlay" class="overlay">
        <img src="./images/5.png" alt="PDF Thumbnail" id="pdfImage" />
    </div>
    <div class="progress-bar-container">
        <div class="progress-bar" id="progressBar"></div>
        <div class="progress-bar-ruler" id="progressBarRuler">
            <div>13,000m</div>
            <div>12,000m</div>
            <div>11,000m</div>
            <div>10,000m</div>
            <div>9,000m</div>
            <div>8,000m</div>
            <div>7,000m</div>
            <div>6,000m</div>
            <div>5,000m</div>
            <div>4,000m</div>
            <div>3,000m</div>
            <div>2,000m</div>
            <div>1,000m</div>
            <div>0m</div>
            <div>수직 발달 구름</div>
        </div>
    </div>
    <div class="progress-bar-container">
        <div class="progress-bar" id="progressBar"></div>
    </div>
    <div class="navbar">
        <a href="#high-clouds">고층운</a>
        <a href="#middle-clouds">중층운</a>
        <a href="#low-clouds">저층운</a>
    </div>
    
    <div class="clouds-container" id="cloudsContainer"></div>
    
    <div class="image-popup" id="imagePopup">
        <img id="popupImage" alt="Cloud Image" />
        <button id="closePopup">닫기</button>
    </div>

    <section id="high-clouds" class="section high-clouds">
        <h1>고층운 (High Clouds)</h1>
        
        <p>고도 약 6,000~13,000m에 위치하며 주로 권운(Cirrus), 권층운(Cirrostratus), 권적운(Cirrocumulus)으로 이루어져 있습니다. 
            얇고 가벼운 특징을 가지고 있으며, 햇빛을 아름답게 산란시킵니다.</p>
        
        <ul>
            <li>
                <div style="text-align: justify; padding-bottom: 50px; padding-top: 40px;">
                    <img src="./images/AdobeStock_234671473.jpg" alt="권운 이미지" style="width: 100%; max-width: 800px; height: auto;">
                <strong>권운 (Cirrus):</strong> 주로 9~13km의 고도에서 나타나며, 구름 입자는 빙정으로 이루어져 있다. 권운은 가늘고 긴 실타래 모양으로 하늘에 퍼져 있고, 햇빛이 통과할 때 하늘이 주황색이나 분홍빛으로 물들며 아침 또는 저녁 노을에 선명하게 보인다.
                대체로 맑고 건조한 날씨에 나타나지만, 권운이 나타난 뒤 시간이 지나면서 하늘을 점차 덮을 경우 온난 전선의 접근을 예고하며 비가 올 가능성이 있다. 권운은 권층운이나 다른 구름이 형성되는 초기 신호로도 인식되며, 
                이후 기후 변화에 따라 비나 눈 같은 강수 현상이 발생할 수 있는 전조 역할을 한다. 얇고 가벼운 털구름이나 머리카락 구름으로 불린다.
            </li>
            <li>
                <div style="text-align: justify; padding-bottom: 50px; padding-top: 40px;">
                    <img src="./images/AdobeStock_117180716.jpg" alt="권운 이미지" style="width: 100%; max-width: 800px; height: auto;">
                <strong>권층운 (Cirrostratus):</strong> 보통 5 ~ 13km의 고도에서 나타나고 구름 입자는 빙정으로 이루어져 있다. 
                햇무리나 달무리를 나타내는 것이 특징이며 초기에 권운이 나타나고 난 6시간 후에 흔히 나타나는 구름이다. 
                엷은 베일처럼 하늘을 뒤덮고, 구름 속에 줄무늬가 보일 때도 있다. 아침 노을이나 저녁 노을로 황색이나 적색을 띤다. 주로 온난전선의 전면에 나타나 다음 날에는 비가 올 징조일 경우가 많다. 그리고 두꺼운 권층운의 경우에는 엷은 고층운과 비슷한 형태를 띠고 있지만 고층운이 약간 진한 색깔을 띄는 일이 많다. 털층구름, 면사포구름, 무리구름이라고도 한다.
            </li>
            <li>
                <div style="text-align: justify; padding-bottom: 50px; padding-top: 40px;">
                    <img src="./images/87.jpg" alt="권운 이미지" style="width: 100%; max-width: 800px; height: auto;">
                <strong>권적운 (Cirrocumulus):</strong> 권운에서 파생된 상층운으로, 잔물결구름 또는 양털구름이라고도 불린다. 
                보통 5~13km의 고도에서 나타나며, 구름 입자는 작은 빙정과 물방울로 구성된다. 권적운은 작은 구름 덩어리들이 물결이나 
                격자 모양으로 퍼져 있는 모습이 특징으로, 대개 맑은 하늘에 얇게 퍼져 빛을 투과할 수 있을 정도로 투명한 경우가 많다.
                
                이 구름은 변화가 잦으며, 보통 추운 공기가 따뜻한 공기 위로 상승할 때 나타난다. 권적운은 대체로 날씨가 좋은 상황에서 관찰되지만, 때로는 갑작스러운 기상 변화를 예고하는 신호로 여겨진다. 아침이나 저녁 햇빛에 의해 붉거나 노란색으로 물들기도 하며, 
                하늘에 얇은 구름 패턴을 만들어내며 독특한 시각적 효과를 연출한다.
                
                
            </li>
        </ul>
    </section>
    
    <section id="middle-clouds" class="section middle-clouds">
        <h1>중층운 (Middle Clouds)</h1>
        <p>고도 약 2,000~6,000m에 위치하며, 대표적으로 고적운(Altocumulus), 고층운(Altostratus)으로 이루어져 있습니다. 얇거나 두꺼운 형태로 햇빛을 약하게 가리거나 투과합니다.</p>
       
        <ul>
            <li>
                <div style="text-align: justify; padding-bottom: 50px; padding-top: 40px;">
                    <img src="./images/89.jpg" alt="권운 이미지" style="width: 100%; max-width: 800px; height: auto;">
                <strong>고적운 (Altocumulus):</strong> 대기 중간층에서 형성되는 구름으로, 
                작은 구름 덩어리들이 모여 배열된 듯한 모양을 가지며 하늘에 퍼져 있는 특징이 있다.
                
                주로 2~7km 고도에서 나타나며, 구름 입자는 물방울과 얼음 결정으로 이루어져 있다. 고적운은 작은 덩어리들이 격자 모양 또는 물결처럼 배열되어 있어 하늘에 무늬를 형성하는데, 덩어리들 사이로 파란 하늘이 드러나기도 한다. 일반적으로 고적운이 나타나는 날씨는 비교적 맑고, 햇빛을 흩어져 은은하게 비추기 때문에 하늘이 온화하게 보인다. 그러나 고적운이 점차 짙어지거나 구름 덩어리가 커질 경우 저기압이 접근하고 있다는 신호로 인식되기도 한다.
            </li>
            <li>
                <div style="text-align: justify; padding-bottom: 50px; padding-top: 40px;">
                    <img src="./images/AdobeStock_596852525.jpg" alt="권운 이미지" style="width: 100%; max-width: 800px; height: auto;">
                <strong>고층운 (Altostratus):</strong> 대기 중간층에서 형성되는 구름으로 넓고 얇은 층 형태로 하늘을 덮는 회색빛 구름이다.
                
                주로 2~7km의 고도에서 나타나며, 구름 입자는 물방울과 얼음 결정으로 이루어져 있다. 고층운은 넓고 균일하게 하늘을 덮으며, 햇빛을 희미하게 투과시켜 하늘이 은은한 회색빛으로 보인다.
                대체로 흐린 날씨에 나타나며, 고층운이 하늘을 점차 두텁게 덮어갈 경우 저기압이나 강수의 징후가 될 수 있다. 고층운은 비나 눈이 내리기 전 단계에서 나타나는 경우가 많아, 날씨 변화의 신호로 인식된다.
                넓고 균일하게 펼쳐진 고층운은 종종 “하늘의 베일”처럼 보이며, 하늘을 온화하고 은은하게 채워준다.
            </li>
        </ul>
    </section>
    
    <section id="low-clouds" class="section low-clouds">
        <h1>저층운 (Low Clouds)</h1>
        <p>고도 약 0~2,000m에 위치하며, 주로 층운(Stratus), 층적운(Stratocumulus), 적운(Cumulus)으로 이루어져 있습니다. 짙은 회색 구름이 자주 나타나며 비나 눈을 동반하는 경우가 많습니다.</p>
        
        <ul>
            <li>
                <div style="text-align: justify; padding-bottom: 50px; padding-top: 40px;">
                    <img src="./images/AdobeStock_990065742.jpg" alt="권운 이미지" style="width: 100%; max-width: 800px; height: auto;">
                <strong>층운 (Stratus):</strong> 낮은 고도에서 나타나는 하층운으로
                안개구름 또는 흐림구름으로도 불린다.
                주로 0 ~ 2km 고도에 걸쳐 나타나며, 구름 입자는 주로 물방울로 이루어져 있다. 하늘을 두텁게 덮어 햇빛을 차단하거나 흐리게 하며, 시야가 제한되는 것이 특징이다. 층운은 안개처럼 낮게 깔려 넓게 퍼져 있으며, 종종 가랑비나 이슬비를 동반하기도 한다. 층운은 가을과 겨울철에 주로 나타나며, 흐린 날씨에 자주 보인다. 이 구름이 짙어지면 하늘이 회색빛을 띠며, 그로 인해 낮은 고도에 흐릿하게 펼쳐진 무겁고 차분한 느낌을 준다.
            </li>
            <li>
                <div style="text-align: justify; padding-bottom: 50px; padding-top: 40px;">
                    <img src="./images/AdobeStock_457012528.jpg" alt="권운 이미지" style="width: 100%; max-width: 800px; height: auto;">
                <strong>층적운 (Stratocumulus):</strong> 낮은 고도에서 나타나는 구름으로, 주로 0 ~ 2km 고도에서 형성되며 하늘에 넓고 둥근 덩어리 모양으로 퍼진다. 층적운은 주로 물방울로 이루어져 있고, 하늘을 회색이나 흰색으로 덮으며, 크고 둥글둥글한 구름 덩어리가 특징이다.

                층적운은 주로 가을과 겨울철에 발생하며, 이 구름이 하늘을 덮으면 햇빛을 약간 가리면서 음영을 형성한다. 
                구름 덩어리가 촘촘히 배열된 모습이 구름의 “이불”처럼 보이기도 하며, 비가 내리기 전 징조로 나타날 때도 있다. 
                층적운은 두꺼운 층을 이루지만 큰 강수를 동반하는 경우는 드물고, 하늘 전체를 덮을 때 흐린 날씨의 특성을 더하는 구름으로 알려져 있다.
            </li>
            <li>
                <div style="text-align: justify; padding-bottom: 50px; padding-top: 40px;">
                    <img src="./images/86.jpg" alt="권운 이미지" style="width: 100%; max-width: 800px; height: auto;">
                <strong>난층운 (nimbostratus cloud):</strong> 난층운은 대기 중 하층에서 넓게 퍼진 회색 구름으로, 고도 약 2,000미터 이하에 주로 형성된다. 이 구름은 비교적 균일한 두께를 가지며, 하늘을 완전히 덮어 일조량을 감소시키는 특징이 있다. 난층운은 수분 함량이 높아 비나 이슬비와 같은 지속적인 강수를 동반하는 경우가 많다. 하단이 두껍고 낮게 위치해 주변 풍경을 뿌옇게 보이게 만들며, 구름 속에 빛이 거의 투과하지 않아 어두운 날씨를 유발한다.

                난층운은 주로 한랭 전선이나 온난 전선의 영향을 받아 형성되며, 수평적인 대기의 안정화로 인해 대류 활동이 적다. 이러한 특성은 비교적 완만한 기상 변화를 나타내는 신호로 간주된다. 항공 운항 시 난층운은 가시거리를 제한하고, 결빙 가능성이 있어 위험 요소로 작용할 수 있다. 난층운의 구조와 형성 메커니즘은 강수 패턴 예측과 기후 모델링에서 중요한 연구 대상으로 여겨지고 있다.
            </li>
        </ul>
    </section>
        <section id="vertical-clouds" class="section vertical-clouds">
            <h1>수직발달 구름 (Vertically Developed Clouds)</h1>
            <p>수직적으로 발달하는 구름으로, 대표적으로 적운(Cumulus), 적란운(Cumulonimbus)으로 이루어져 있습니다. 대기 불안정으로 인해 형성되며 강수와 뇌우를 동반하는 경우가 많습니다.</p>
            
            <ul>
                <li>
                    <div style="text-align: justify; padding-bottom: 50px; padding-top: 40px;">
                        <img src="./images/85.jpg" alt="권운 이미지" style="width: 100%; max-width: 800px; height: auto;">
                    <strong>적운 (Cumulus):</strong> 낮은 고도에서 형성되는 구름으로, 주로 500~2,000미터 고도에서 나타나며 뭉게뭉게 피어오르는 덩어리 모양이 특징이다. 적운은 주로 물방울로 이루어져 있으며, 맑은 날씨에 하얗고 두툼한 구름 덩어리들이 하늘에 산재해 있는 모습으로 관찰된다.

                    적운은 대개 여름철에 활발히 발생하며, 강한 열로 인해 공기가 빠르게 상승하면서 형성된다. 이 구름은 기저가 평평하고 윗부분이 부드러운 곡선 형태로 솟아올라, 특유의 둥근 모양을 이루게 된다. 적운은 대체로 날씨 변화와 관계없이 맑은 하늘을 배경으로 볼 수 있지만, 가끔 구름이 짙어지고 위로 크게 발달할 경우 소나기나 천둥번개의 징후로 발전할 수 있다. 적운은 따뜻한 날씨를 나타내며, 구름 덩어리들이 하늘에 자연스럽게 흩어져 있어 “양털 구름”이라 불리기도 한다.
                </li>
                <li>
                    <div style="text-align: justify; padding-bottom: 50px; padding-top: 40px;">
                        <img src="./images/84.jpg" alt="권운 이미지" style="width: 100%; max-width: 800px; height: auto;">
                    <strong>적란운 (Cumulonimbus):</strong> 강한 상승 기류에 의해 형성된 거대한 수직 구름으로, 고도 약 500~16,000미터에 이르는 층으로 발달할 수 있다. 적란운은 물방울과 얼음 결정이 함께 존재하며, 하단은 평평하고 상단이 모자처럼 퍼진 형태가 특징이다. 주로 대류가 활발한 여름철에 발생하며, 번개와 천둥, 폭우를 동반할 때가 많다. 적란운이 나타나면 갑작스러운 날씨 변화의 전조로 여겨진다. 적란운은 그 형성 과정에서 대류 활동이 극대화되며, 강한 상승 기류로 인해 내부에서 물방울과 얼음 결정이 끊임없이 충돌하면서 정전기가 발생한다. 이는 번개와 천둥을 유발하는 주요 원인이 된다. 또한 적란운은 기상학적으로 매우 중요한 연구 대상인데, 그 이유는 강력한 폭풍우, 토네이도, 혹은 우박을 동반하는 극한 날씨와 밀접하게 연결되어 있기 때문이다. 이러한 특징 때문에 적란운은 항공 운항 시 위험 요소로 여겨지며, 관측 및 예측 기술을 통해 피해를 최소화하려는 노력이 이어지고 있다.
                </li>
            </ul>
    </section>
    

<style>
     /* 페이드 인 효과 추가 */
     .overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 2000;
            opacity: 0; /* 초기 상태 투명 */
            visibility: hidden; /* 초기 상태 숨김 */
            transition: opacity 1s ease; /* 페이드 인 효과 */
        }

        .overlay.show {
            opacity: 1; /* 불투명 */
            visibility: visible; /* 보임 */
        }
    .overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgb(255, 255, 255);
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 2000;
    transition: opacity 1s ease; /* 페이드 아웃 효과 */
    opacity: 1;
    pointer-events: auto;
}

.overlay img {
    max-width: 90%;
    max-height: 90%;
    cursor: pointer;
}

.overlay.hidden {
    opacity: 0;
    pointer-events: none; /* 클릭 방지 */
}
    /* 눈금자 스타일 */
.progress-bar-ruler {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 10px; /* 숫자 크기를 줄임 */
    color: white;
    pointer-events: none; /* 클릭 방지 */
    overflow: hidden; /* 넘치는 부분 숨김 */
    padding: 0 5px; /* 양쪽 여백 추가 */
    box-sizing: border-box; /* 패딩 포함 크기 계산 */
}

.progress-bar-ruler div {
    position: relative;
    transform: translateX(-50%);
    white-space: nowrap; /* 텍스트가 줄 바꿈되지 않도록 설정 */
    font-size: 0.9em; /* 텍스트 크기를 조절 */
}
    .footer {
        position: fixed;
        bottom: 0;
        width: 100%;
        background: rgba(132, 189, 246, 0.818);
        padding: 10px 0;
        text-align: center;
        z-index: 1000;
    }

    .footer a {
        color: white;
        margin: 0 15px;
        text-decoration: none;
        font-weight: bold;
        font-size: 1.2em;
    }

    .footer a:hover {
        text-decoration: underline;
    }
</style>

<footer class="footer">
    <a href="#" id="constable">존 커스터블</a>
    <a href="#" id="shinkai">신카이 마코토</a>
    <a href="#" id="koreeda">고레에다 히로카즈</a>
    <a href="#" id="miyazaki">미야자키 하야오</a>
    <a href="#" id="sungyul">성률</a>
    <a href="#" id="hosoda">호소다 마모루</a>
</footer>
    </footer>

    <script>
      // 작가 이름과 PDF 경로 매핑
      const pdfMap = {
        constable: './pdfs/constable.pdf',
        shinkai: './pdfs/shinkai.pdf',
        koreeda: './pdfs/koreeda.pdf',
        miyazaki: './pdfs/miyazaki.pdf',
        sungyul: './pdfs/sungyul.pdf',
        hosoda: './pdfs/hosoda.pdf'
    };
// 각 링크에 클릭 이벤트 추가
document.querySelectorAll('.footer a').forEach(link => {
        link.addEventListener('click', function (event) {
            event.preventDefault(); // 기본 동작 방지
            const pdfUrl = pdfMap[this.id]; // 링크의 id로 PDF URL 찾기
            if (pdfUrl) {
                window.open(pdfUrl, '_blank'); // 새 창에서 PDF 열기
            } else {
                alert('PDF를 찾을 수 없습니다.');
            }
        });
    });
    document.addEventListener('DOMContentLoaded', () => {
        const cloudsContainer = document.getElementById('cloudsContainer');

        // PNG 이미지 경로 리스트
        const cloudImages = [
            './images/78.png',
            './images/79.png',
            './images/80.png',
            './images/81.png',
            './images/82.png',
            './images/83.png',
        ];

        function createRandomCloud() {
            const cloud = document.createElement('div');
            cloud.classList.add('cloud');

            // 랜덤 이미지 선택
            const randomImage = cloudImages[Math.floor(Math.random() * cloudImages.length)];
            cloud.style.backgroundImage = `url(${randomImage})`;

            // 랜덤 위치와 크기 설정
            const size = Math.random() * 100 + 50; // 50px ~ 150px
            cloud.style.width = `${size}px`;
            cloud.style.height = `${size / 1.5}px`;
            cloud.style.top = `${Math.random() * 80}vh`;
            cloud.style.left = `${Math.random() * 100}vw`;
            cloud.style.animationDuration = `${Math.random() * 30 + 20}s`;

            cloudsContainer.appendChild(cloud);

            setTimeout(() => {
                cloud.remove();
            }, 30000); // 애니메이션 시간 후 삭제
        }

        // 구름 생성 주기
        setInterval(createRandomCloud, 2000);

        // 초기 구름 생성
        for (let i = 0; i < 5; i++) createRandomCloud();
    });
    </script>
</body>
    <script>
        document.addEventListener('DOMContentLoaded', () => {
    const overlay = document.getElementById('pdfOverlay');
    const pdfImage = document.getElementById('pdfImage');

    pdfImage.addEventListener('click', () => {
        overlay.classList.add('hidden'); // 페이드 아웃 효과를 추가
        setTimeout(() => {
            overlay.style.display = 'none'; // 페이드 아웃 후 오버레이 숨김
        }, 1000); // CSS transition 시간과 동일하게 설정
    });
});
        const cloudTexts = [
          'Cloud',
'Nube',
'Nuage',
'Wolke',
'Nuvola',
'Nuvem',
'Облако',
'Mây',
'Cumulus',
'Oblak',
'구름',
'云',
'雲',
'Awan',
'Megha',
'Chmura',
'Felhő',
'Nebula',
'Clò',
'Chmurka',
'Kumo',
'Altocumulus',
'Skyen',
'Helwa',
'Nephos',
'Nubo',
'Pēra',
'Magua',
'Enxada',
'Skya',
'Piovra',
'Céu',
'Himmel',
'Zeru',
'Langit',
'Magla',
'Verð',
'Māra',
'Oblaka'
        ];
        const cloudImageMap = {
            'Cloud': './images/8.png',
    'Nube': './images/9.png',
    'Nuage': './images/10.png',
    'Wolke': './images/11.png',
    'Nuvola': './images/12.png',
    'Nuvem': './images/13.png',
    'Облако': './images/14.png',
    'Mây': './images/15.png',
    'Cumulus': './images/16.png',
    'Oblak': './images/17.png',
    '구름': './images/18.png',
    '云': './images/19.png',
    '雲': './images/20.png',
    'Awan': './images/21.png',
    'Megha': './images/22.png',
    'Chmura': './images/23.png',
    'Felhő': './images/24.png',
    'Nebula': './images/25.png',
    'Clò': './images/26.png',
    'Chmurka': './images/27.png',
    'Kumo': './images/28.png',
    'Altocumulus': './images/29.png',
    'Skyen': './images/30.png',
    'Helwa': './images/31.png',
    'Nephos': './images/32.png',
    'Nubo': './images/33.png',
    'Pēra': './images/34.png',
    'Magua': './images/35.png',
    'Enxada': './images/36.png',
    'Skya': './images/37.png',
    'Piovra': './images/38.png',
    'Céu': './images/39.png',
    'Himmel': './images/40.png',
    'Zeru': './images/41.png',
    'Langit': './images/42.png',
    'Magla': './images/43.png',
    'Verð': './images/44.png',
    'Māra': './images/45.png',
    'Oblaka': './images/46.png'
};

    
        // Show the popup with the corresponding image
        function showImage(cloudText) {
            const imageUrl = cloudImageMap[cloudText];
            if (imageUrl) {
                popupImage.src = imageUrl;
                imagePopup.style.display = 'block';
            }
        }

        // Close the popup
        closePopup.addEventListener('click', () => {
            imagePopup.style.display = 'none';
            popupImage.src = '';
        });

        // Create a random cloud
        function createRandomCloud() {
            const cloud = document.createElement('div');
            cloud.classList.add('cloud');

            // Random size
            const size = Math.random() * 150 + 100; // 100px ~ 250px
            cloud.style.width = `${size}px`;
            cloud.style.height = `${size / 2}px`;

            // Random position
            const topPosition = Math.random() * 80; // Within viewport height
            cloud.style.top = `${topPosition}vh`;
            cloud.style.left = `${Math.random() * 100}vw`;
            cloud.style.animationDuration = `${Math.random() * 30 + 20}s`;

            // Assign a random text
            const randomText = cloudTexts[Math.floor(Math.random() * cloudTexts.length)];
            cloud.textContent = randomText;
            cloud.style.display = 'flex';
            cloud.style.alignItems = 'center';
            cloud.style.justifyContent = 'center';
            cloud.style.fontSize = '14px';
            cloud.style.color = 'white';

            // Add click event
            cloud.addEventListener('click', () => showImage(randomText));

            cloudsContainer.appendChild(cloud);

            // Remove cloud after animation ends
            setTimeout(() => {
                cloud.remove();
            }, 30000); // Match the animation duration
        }

        // Generate clouds every 2 seconds
        setInterval(createRandomCloud, 2000);

        // Generate initial clouds on load
        window.addEventListener('load', () => {
            for (let i = 0; i < 5; i++) createRandomCloud();
        });
        // JavaScript: 스크롤 진행률 계산 및 업데이트
window.addEventListener('scroll', () => {
    const scrollTop = window.scrollY; // 현재 스크롤 위치
    const docHeight = document.body.scrollHeight - window.innerHeight; // 전체 스크롤 가능 거리
    const scrollPercent = (scrollTop / docHeight) * 100; // 스크롤 진행률 계산

    const progressBar = document.getElementById('progressBar');
    progressBar.style.width = `${scrollPercent}%`; // 진행 바 너비 업데이트
});
setTimeout(() => {
                pdfOverlay.classList.add("show");
            }, 100); // 약간의 지연시간을 두고 실행

            // 이미지를 클릭하면 페이드 아웃 효과로 페이지 전환
            pdfOverlay.addEventListener("click", () => {
                pdfOverlay.style.transition = "opacity 1s ease";
                pdfOverlay.style.opacity = "0";
                setTimeout(() => {
                    pdfOverlay.style.display = "none"; // 완전히 숨김
                }, 1000); // 페이드 아웃 후 숨기기
            });
    </script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/pdf.js/2.16.105/pdf.min.js"></script>
    <script>
    document.addEventListener("DOMContentLoaded", () => {
    const pdfViewerOverlay = document.getElementById("pdfViewerOverlay");
    const pdfCanvas = document.getElementById("pdfCanvas");
    const closePdfViewer = document.getElementById("closePdfViewer");
    const footerLinks = document.querySelectorAll(".footer a");

    const pdfjsLib = window["pdfjs-dist/build/pdf"];
    pdfjsLib.GlobalWorkerOptions.workerSrc = "https://cdnjs.cloudflare.com/ajax/libs/pdf.js/2.16.105/pdf.worker.min.js";

    let pdfDoc = null;
    let pageNum = 1;
    const ctx = pdfCanvas.getContext("2d");

    // PDF 페이지 렌더링
    function renderPage(num) {
        pdfDoc.getPage(num).then((page) => {
            const viewport = page.getViewport({ scale: 1.5 });
            pdfCanvas.height = viewport.height;
            pdfCanvas.width = viewport.width;

            const renderContext = {
                canvasContext: ctx,
                viewport: viewport,
            };
            page.render(renderContext);
        });
    }

    // PDF 로드
    function loadPdf(url) {
        pdfjsLib.getDocument(url).promise.then((doc) => {
            pdfDoc = doc;
            pageNum = 1;
            renderPage(pageNum);
        });
    }

    // Footer 링크 클릭 이벤트
    footerLinks.forEach((link) => {
        link.addEventListener("click", (e) => {
            e.preventDefault();
            const pdfUrl = link.getAttribute("data-pdf");
            if (pdfUrl) {
                loadPdf(pdfUrl);
                pdfViewerOverlay.classList.add("show");
                pdfViewerOverlay.style.pointerEvents = "auto"; // PDF Viewer 활성화
            }
        });
    });

    // PDF Viewer 닫기 버튼
    closePdfViewer.addEventListener("click", () => {
        pdfViewerOverlay.classList.remove("show");
        setTimeout(() => {
            pdfViewerOverlay.style.pointerEvents = "none"; // PDF Viewer 비활성화
        }, 300); // 충분히 짧은 시간으로 설정
    });
});

    </script>   
    <!-- PDF Viewer Overlay -->
<div id="pdfViewerOverlay">
    <div id="pdfViewerContainer">
        <canvas id="pdfCanvas"></canvas>
        <button id="closePdfViewer">닫기</button>
    </div>
</div>
</body>
</html>
