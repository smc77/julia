cmake_minimum_required(VERSION 2.8)
project(libm387)

enable_language(ASM)

set(CMAKE_ASM_FLAGS_RELEASE -m32 -fPIC)
set(CMAKE_ASM_FLAGS_RELEASE -m32 -fPIC)

set(CMAKE_SHARED_LINKER_FLAGS -nostdlib -m32)

set(SOURCES e_exp.S
e_fmod.S
e_log.S
e_log10.S
e_log10f.S
e_logf.S
e_remainder.S
e_remainderf.S
e_remainderl.S
e_sqrt.S
e_sqrtf.S
e_sqrtl.S
s_ceil.S
s_ceilf.S
s_ceill.S
s_copysign.S
s_copysignf.S
s_copysignl.S
s_cos.S
s_fabs.S
s_fabsf.S
s_finite.S
s_floor.S
s_floorf.S
s_floorl.S
s_llrint.S
s_llrintf.S
s_llrintl.S
s_logb.S
s_logbf.S
s_logbl.S
s_lrint.S
s_lrintf.S
s_lrintl.S
s_remquo.S
s_remquof.S
s_remquol.S
s_rint.S
s_rintf.S
s_rintl.S
s_scalbn.S
s_scalbnf.S
s_scalbnl.S
s_significand.S
s_significandf.S
s_sin.S
s_tan.S
s_trunc.S
s_truncf.S
s_truncl.S
)

add_library(libm387 SHARED ${SOURCES})