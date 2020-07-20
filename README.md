<details>
<summary>Original README.md</summary>
<div markdown="1">

# 개요

https://www.ispyconnect.com/

iSpy is the world’s most popular open source video surveillance application. It's compatible with the the vast majority of consumer webcams and IP cameras. With more than 2 million users worldwide, iSpy works with more cameras and devices than anything else on the market.

![iSpyInterface](https://www.ispyconnect.com/content/ebook/ispysurface.jpg)

## Agent
We have a new platform called Agent which runs as a service and has a full local and remote UI that works on all devices and doesn't require port forwarding for remote access. We've added everything in iSpy plus a lot more to Agent. Check it out on our downloads page

https://www.ispyconnect.com/download.aspx

## About iSpy

Started back in 2007 the software has continually evolved and improved to become a robust, feature rich solution.

The number one use of iSpy is small business security, but home monitoring, neighborhood watch, checking in on the kids, desktop monitoring and mobile access through a iSpyConnect.com are valued features.

Facial recognition and detection of changes in lighting and audio offer the subtleties that set the software apart from competitors.

Getting started with iSpy is easy: all you need is a webcam or IP camera connected to your computer or network.

iSpy connects to the camera and shows the live view. You can then define specific areas of the video that iSpy should watch for movement, and set a threshold value for the amount of motion that would trigger automatic recording. iSpy can also operate in always-recording or manual-recording modes and supports scheduling and remote access (with an iSpyConnect subscription)

iSpy was designed to provide a low-cost alternative to expensive surveillance systems. It has become a highly scalable application that can be tailored to record and take actions on specific incidents as defined by the user either locally or remotely.

## Installing iSpy

https://www.ispyconnect.com/download.aspx

## Compiling iSpy
The solution requires **Visual Studio 2019** to build. Choose 32 or 64 bit version to build.

For building the Setup project [Wix Toolset 3.11](http://wixtoolset.org/) must be installed. (Make sure you restart Visual Studio after installing)

To build the full installer select x86 or x64 Release mode and compile the Bootstrap project. Installer will be generated in  
Wix\Bootstrap\bin\Release

***Remove the signing post build event command as the code signing certificate is not part of the source code of the project.***

If you have dll reference errors when building you may need to go into the DLLS folder and right-click - unblock the DLLs. (Windows Security issue)



</div>
</details>

## 컴파일 설정

> #### Requirement
>> Visual Studio 2019
>>
>> [Wix Toolset 3.11.* + VS 2019 Extention](http://wixtoolset.org/) (설치 후 Visual Studio를 다시 시작해야 합니다.)

> ### 윈도우 환경에서 컴파일 하기
>```
>1.Visual Studio 2019 설치(.net 4.5 FrameWorks for C# 포함)
>2.Wix Toolset 및 Visual Studio 2019 확장 설치
>3.소스코드 다운로드 (https://github.com/ispysoftware/iSpy)
>4.iSpy.sln 솔루션 VS 2019로 열기
>5.x86/x64 선택후 Release 모드로 변경
>6.Bootstrap, iSpy, iSpyMonitor, iSpySetup, WixCA 5개의 프로젝트에서 빌드 이벤트 제거
>```
>설치 프로그램 생성위치 : %Solution% \ Wix \ Bootstrap \ bin \ Release
>
>실행 프로그램(iSpy) 생성위치 : %Solution% \ bin \ x86/x64 \ Release
>
>****
>*빌드시에 dll참조 오류가 발생하면 DLLS 폴더로 이동하여 마우스 오른쪽 버튼을 클릭한 뒤, DLL 차단을 해제하여야 합니다.*
>
>*실행 프로그램(iSpy) 빌드위치의 파일을 삭제한 이후에 다시 빌드할 경우, %Solution% \ DLLS의 파일을 생성위치에 복사해야 합니다.*
>
>*DEBUG 모드로 프로젝트를 빌드하여 실행할 경우 성능저하 문제가 있습니다.*




