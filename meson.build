project('VirtualSwapchainLayer', 'cpp',
  license: 'apache',
  version: '0.10.0',
)

dependencies = [
  dependency('threads')
]

sources = [
  'base_swapchain.cpp',
  'layer.cpp',
  'platform.cpp',
  'swapchain.cpp',
  'virtual_swapchain.cpp'
]

lib = shared_library('VkLayer_VirtualSwapchain', sources,
  dependencies: dependencies,
  gnu_symbol_visibility: 'hidden',
  install: true,
)

soname = lib.full_path().split('/')[-1]
conf = configuration_data()
conf.set_quoted('library', get_option('prefix') / get_option('libdir') / soname)

configure_file(
  input: 'VirtualSwapchainLayer.json',
  output: 'VirtualSwapchainLayer.json',
  configuration: conf,
  install_dir: 'share/vulkan/explicit_layer.d',
  install: true
)
