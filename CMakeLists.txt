cmake_minimum_required(VERSION 3.28)
project(BasicAudioAnalysis)

set(CMAKE_CXX_STANDARD 17)

find_package(portaudio CONFIG REQUIRED)
find_package(FFTW3 CONFIG REQUIRED)


add_executable(BasicAudioAnalysis main.cpp)
target_include_directories(BasicAudioAnalysis PRIVATE ${PORTAUDIO_INCLUDE_DIRS})
target_include_directories(BasicAudioAnalysis PRIVATE ${FFTW3_INCLUDE_DIRS})
target_link_libraries(BasicAudioAnalysis PRIVATE portaudio_static)
target_link_libraries(BasicAudioAnalysis PRIVATE FFTW3::fftw3)
