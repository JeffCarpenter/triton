add_triton_library(TritonGPUToLLVM
    ConvertLayoutOpToLLVM/SharedToDotOperandFMA.cpp
    DotOpToLLVM/FMA.cpp
    ElementwiseOpToLLVM.cpp
    MemoryOpToLLVM.cpp
    AssertOpToLLVM.cpp
    ViewOpToLLVM.cpp
    MakeRangeOpToLLVM.cpp
    TypeConverter.cpp
    Utility.cpp

    LINK_LIBS PUBLIC
    MLIRIR
    MLIRPass
    MLIRGPUDialect
    MLIRGPUToNVVMTransforms
    MLIRGPUToROCDLTransforms
    MLIRGPUTransforms
    TritonAnalysis
    TritonIR
    TritonGPUIR
    TritonGPUTransforms
    TritonNvidiaGPUTransforms
    NVGPUIR
)
