- Building
```shell
cmake -S . -B build -G Ninja
cmake --build build/
```


- Output from `cmake -S . -B build -G Ninja`
```shell
-- The C compiler identification is GNU 12.2.0
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Check for working C compiler: /usr/bin/cc - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Looking for CL_VERSION_3_0
-- Looking for CL_VERSION_3_0 - found
-- Found OpenCL: /usr/lib/libOpenCL.so (found version "3.0")
-- Found OpenGL: /usr/lib/libOpenGL.so
-- Configuring done (0.4s)
-- Generating done (0.0s)
-- Build files have been written to: /home/schmidh/Gitrepos/OpenCL-GL-Interop/build
```

- Running
```shell
./build/glfwBasicInterop
```

- Output
```shell
Error Code: -1000
Couldn't create a context.
```

- Error Code
```
-1000 ⇒ CL_INVALID_GL_SHAREGROUP_REFERENCE_KHR
```

- OpenCl Info
```shell
clinfo
> excerpt:
> Platform Name                   NVIDIA CUDA
> Platform Vendor                 NVIDIA Corporation
> Platform Version                OpenCL 3.0 CUDA 12.2.148
> Platform Profile                FULL_PROFILE
> ...
> Device Name                     Quadro P400
> Device Vendor                   NVIDIA Corporation
> Device Vendor ID                0x10de
> Device Version                  OpenCL 3.0 CUDA
> Device UUID                     950084ee-ae71-7179-d84f-c4a5286f163d
> Driver UUID                     950084ee-ae71-7179-d84f-c4a5286f163d
> Valid Device LUID               No
> Device LUID                     6d69-637300000000
> Device Node Mask                0
> Device Numeric Version          0xc00000 (3.0.0)
> Driver Version                  535.146.02
> Device OpenCL C Version         OpenCL C 1.2
> Device OpenCL C all versions    OpenCL C 0x400000 (1.0.0)
>                                 OpenCL C 0x401000 (1.1.0)
>                                 OpenCL C 0x402000 (1.2.0)
>                                 OpenCL C 0xc00000 (3.0.0)
> ...
> Platform Extensions             cl_khr_gl_sharing 0x400000 (1.0.0)
> Device Extensions               cl_khr_gl_sharing 0x400000 (1.0.0)
```
