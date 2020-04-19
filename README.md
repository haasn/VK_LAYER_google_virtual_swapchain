# VK_LAYER_google_virtual_swapchain

Copy/pasted from
[google/agi](https://github.com/google/agi/tree/master/core/vulkan/vk_virtual_swapchain/cc) into a new project, with added
meson build scripts and some minor changes.

## Why?

Because I didn't know about
[`vkCreateHeadlessSurfaceEXT`](https://www.khronos.org/registry/vulkan/specs/1.2-extensions/man/html/vkCreateHeadlessSurfaceEXT.html) at the time of making this project. It's useless. Just use that instead.
