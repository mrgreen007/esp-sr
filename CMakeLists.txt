set(COMPONENT_SRCS
    speech_command_recognition/mn_process_commands.c
    )

set(COMPONENT_ADD_INCLUDEDIRS 
    lib/include
    wake_word_engine/include
    speech_command_recognition/include
    acoustic_algorithm/include
    )


register_component()

target_link_libraries(${COMPONENT_NAME} "-L ${CMAKE_CURRENT_SOURCE_DIR}/lib")
target_link_libraries(${COMPONENT_NAME} "-L ${CMAKE_CURRENT_SOURCE_DIR}/wake_word_engine")
target_link_libraries(${COMPONENT_NAME} "-L ${CMAKE_CURRENT_SOURCE_DIR}/speech_command_recognition")
target_link_libraries(${COMPONENT_NAME} "-L ${CMAKE_CURRENT_SOURCE_DIR}/acoustic_algorithm")
target_link_libraries(${COMPONENT_NAME} 
    dl_lib
    c_speech_features
    wakenet
    hilexin_wn3
    hilexin_wn4
    hilexin_wn5
    hilexin_wn5X2
    hilexin_wn5X3
    customized_word_wn5
    customized_word_wn6
    nihaoxiaozhi_wn5
    nihaoxiaozhi_wn5X2
    nihaoxiaoxin_wn6
    multinet
    multinet1_ch
    esp_audio_processor
    )

