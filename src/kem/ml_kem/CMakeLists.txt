# SPDX-License-Identifier: MIT

# This file was generated by
# scripts/copy_from_upstream/copy_from_upstream.py

set(_ML_KEM_OBJS "")

if(OQS_ENABLE_KEM_ml_kem_512)
    add_library(ml_kem_512_ref OBJECT kem_ml_kem_512.c pqcrystals-kyber-standard_ml-kem-512_ref/cbd.c pqcrystals-kyber-standard_ml-kem-512_ref/indcpa.c pqcrystals-kyber-standard_ml-kem-512_ref/kem.c pqcrystals-kyber-standard_ml-kem-512_ref/ntt.c pqcrystals-kyber-standard_ml-kem-512_ref/poly.c pqcrystals-kyber-standard_ml-kem-512_ref/polyvec.c pqcrystals-kyber-standard_ml-kem-512_ref/reduce.c pqcrystals-kyber-standard_ml-kem-512_ref/symmetric-shake.c pqcrystals-kyber-standard_ml-kem-512_ref/verify.c)
    target_compile_options(ml_kem_512_ref PUBLIC -DKYBER_K=2)
    target_include_directories(ml_kem_512_ref PRIVATE ${CMAKE_CURRENT_LIST_DIR}/pqcrystals-kyber-standard_ml-kem-512_ref)
    target_include_directories(ml_kem_512_ref PRIVATE ${PROJECT_SOURCE_DIR}/src/common/pqclean_shims)
    target_compile_options(ml_kem_512_ref PUBLIC -DKYBER_K=2)
    set(_ML_KEM_OBJS ${_ML_KEM_OBJS} $<TARGET_OBJECTS:ml_kem_512_ref>)
endif()

if(OQS_ENABLE_KEM_ml_kem_512_avx2)
    add_library(ml_kem_512_avx2 OBJECT pqcrystals-kyber-standard_ml-kem-512_avx2/basemul.S pqcrystals-kyber-standard_ml-kem-512_avx2/cbd.c pqcrystals-kyber-standard_ml-kem-512_avx2/consts.c pqcrystals-kyber-standard_ml-kem-512_avx2/fq.S pqcrystals-kyber-standard_ml-kem-512_avx2/indcpa.c pqcrystals-kyber-standard_ml-kem-512_avx2/invntt.S pqcrystals-kyber-standard_ml-kem-512_avx2/kem.c pqcrystals-kyber-standard_ml-kem-512_avx2/ntt.S pqcrystals-kyber-standard_ml-kem-512_avx2/poly.c pqcrystals-kyber-standard_ml-kem-512_avx2/polyvec.c pqcrystals-kyber-standard_ml-kem-512_avx2/rejsample.c pqcrystals-kyber-standard_ml-kem-512_avx2/shuffle.S pqcrystals-kyber-standard_ml-kem-512_avx2/symmetric-shake.c pqcrystals-kyber-standard_ml-kem-512_avx2/verify.c)
    target_include_directories(ml_kem_512_avx2 PRIVATE ${CMAKE_CURRENT_LIST_DIR}/pqcrystals-kyber-standard_ml-kem-512_avx2)
    target_include_directories(ml_kem_512_avx2 PRIVATE ${PROJECT_SOURCE_DIR}/src/common/pqclean_shims)
    target_compile_options(ml_kem_512_avx2 PRIVATE  -mavx2  -mbmi2  -mpopcnt )
    target_compile_options(ml_kem_512_avx2 PUBLIC -DKYBER_K=2)
    set(_ML_KEM_OBJS ${_ML_KEM_OBJS} $<TARGET_OBJECTS:ml_kem_512_avx2>)
endif()

if(OQS_ENABLE_KEM_ml_kem_768)
    add_library(ml_kem_768_ref OBJECT kem_ml_kem_768.c pqcrystals-kyber-standard_ml-kem-768_ref/cbd.c pqcrystals-kyber-standard_ml-kem-768_ref/indcpa.c pqcrystals-kyber-standard_ml-kem-768_ref/kem.c pqcrystals-kyber-standard_ml-kem-768_ref/ntt.c pqcrystals-kyber-standard_ml-kem-768_ref/poly.c pqcrystals-kyber-standard_ml-kem-768_ref/polyvec.c pqcrystals-kyber-standard_ml-kem-768_ref/reduce.c pqcrystals-kyber-standard_ml-kem-768_ref/symmetric-shake.c pqcrystals-kyber-standard_ml-kem-768_ref/verify.c)
    target_compile_options(ml_kem_768_ref PUBLIC -DKYBER_K=3)
    target_include_directories(ml_kem_768_ref PRIVATE ${CMAKE_CURRENT_LIST_DIR}/pqcrystals-kyber-standard_ml-kem-768_ref)
    target_include_directories(ml_kem_768_ref PRIVATE ${PROJECT_SOURCE_DIR}/src/common/pqclean_shims)
    target_compile_options(ml_kem_768_ref PUBLIC -DKYBER_K=3)
    set(_ML_KEM_OBJS ${_ML_KEM_OBJS} $<TARGET_OBJECTS:ml_kem_768_ref>)
endif()

if(OQS_ENABLE_KEM_ml_kem_768_avx2)
    add_library(ml_kem_768_avx2 OBJECT pqcrystals-kyber-standard_ml-kem-768_avx2/basemul.S pqcrystals-kyber-standard_ml-kem-768_avx2/cbd.c pqcrystals-kyber-standard_ml-kem-768_avx2/consts.c pqcrystals-kyber-standard_ml-kem-768_avx2/fq.S pqcrystals-kyber-standard_ml-kem-768_avx2/indcpa.c pqcrystals-kyber-standard_ml-kem-768_avx2/invntt.S pqcrystals-kyber-standard_ml-kem-768_avx2/kem.c pqcrystals-kyber-standard_ml-kem-768_avx2/ntt.S pqcrystals-kyber-standard_ml-kem-768_avx2/poly.c pqcrystals-kyber-standard_ml-kem-768_avx2/polyvec.c pqcrystals-kyber-standard_ml-kem-768_avx2/rejsample.c pqcrystals-kyber-standard_ml-kem-768_avx2/shuffle.S pqcrystals-kyber-standard_ml-kem-768_avx2/symmetric-shake.c pqcrystals-kyber-standard_ml-kem-768_avx2/verify.c)
    target_include_directories(ml_kem_768_avx2 PRIVATE ${CMAKE_CURRENT_LIST_DIR}/pqcrystals-kyber-standard_ml-kem-768_avx2)
    target_include_directories(ml_kem_768_avx2 PRIVATE ${PROJECT_SOURCE_DIR}/src/common/pqclean_shims)
    target_compile_options(ml_kem_768_avx2 PRIVATE  -mavx2  -mbmi2  -mpopcnt )
    target_compile_options(ml_kem_768_avx2 PUBLIC -DKYBER_K=3)
    set(_ML_KEM_OBJS ${_ML_KEM_OBJS} $<TARGET_OBJECTS:ml_kem_768_avx2>)
endif()

if(OQS_ENABLE_KEM_ml_kem_1024)
    add_library(ml_kem_1024_ref OBJECT kem_ml_kem_1024.c pqcrystals-kyber-standard_ml-kem-1024_ref/cbd.c pqcrystals-kyber-standard_ml-kem-1024_ref/indcpa.c pqcrystals-kyber-standard_ml-kem-1024_ref/kem.c pqcrystals-kyber-standard_ml-kem-1024_ref/ntt.c pqcrystals-kyber-standard_ml-kem-1024_ref/poly.c pqcrystals-kyber-standard_ml-kem-1024_ref/polyvec.c pqcrystals-kyber-standard_ml-kem-1024_ref/reduce.c pqcrystals-kyber-standard_ml-kem-1024_ref/symmetric-shake.c pqcrystals-kyber-standard_ml-kem-1024_ref/verify.c)
    target_compile_options(ml_kem_1024_ref PUBLIC -DKYBER_K=4)
    target_include_directories(ml_kem_1024_ref PRIVATE ${CMAKE_CURRENT_LIST_DIR}/pqcrystals-kyber-standard_ml-kem-1024_ref)
    target_include_directories(ml_kem_1024_ref PRIVATE ${PROJECT_SOURCE_DIR}/src/common/pqclean_shims)
    target_compile_options(ml_kem_1024_ref PUBLIC -DKYBER_K=4)
    set(_ML_KEM_OBJS ${_ML_KEM_OBJS} $<TARGET_OBJECTS:ml_kem_1024_ref>)
endif()

if(OQS_ENABLE_KEM_ml_kem_1024_avx2)
    add_library(ml_kem_1024_avx2 OBJECT pqcrystals-kyber-standard_ml-kem-1024_avx2/basemul.S pqcrystals-kyber-standard_ml-kem-1024_avx2/cbd.c pqcrystals-kyber-standard_ml-kem-1024_avx2/consts.c pqcrystals-kyber-standard_ml-kem-1024_avx2/fq.S pqcrystals-kyber-standard_ml-kem-1024_avx2/indcpa.c pqcrystals-kyber-standard_ml-kem-1024_avx2/invntt.S pqcrystals-kyber-standard_ml-kem-1024_avx2/kem.c pqcrystals-kyber-standard_ml-kem-1024_avx2/ntt.S pqcrystals-kyber-standard_ml-kem-1024_avx2/poly.c pqcrystals-kyber-standard_ml-kem-1024_avx2/polyvec.c pqcrystals-kyber-standard_ml-kem-1024_avx2/rejsample.c pqcrystals-kyber-standard_ml-kem-1024_avx2/shuffle.S pqcrystals-kyber-standard_ml-kem-1024_avx2/symmetric-shake.c pqcrystals-kyber-standard_ml-kem-1024_avx2/verify.c)
    target_include_directories(ml_kem_1024_avx2 PRIVATE ${CMAKE_CURRENT_LIST_DIR}/pqcrystals-kyber-standard_ml-kem-1024_avx2)
    target_include_directories(ml_kem_1024_avx2 PRIVATE ${PROJECT_SOURCE_DIR}/src/common/pqclean_shims)
    target_compile_options(ml_kem_1024_avx2 PRIVATE  -mavx2  -mbmi2  -mpopcnt )
    target_compile_options(ml_kem_1024_avx2 PUBLIC -DKYBER_K=4)
    set(_ML_KEM_OBJS ${_ML_KEM_OBJS} $<TARGET_OBJECTS:ml_kem_1024_avx2>)
endif()

set(ML_KEM_OBJS ${_ML_KEM_OBJS} PARENT_SCOPE)
