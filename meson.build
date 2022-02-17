project('concurencpp', 'cpp', default_options: 
'cpp_std=c++20')

concurecpp_inc = include_directories([
  'include'
])

concurecpp_lib = static_library('concurencpp', [
  'source/executors/executor.cpp',
  'source/executors/manual_executor.cpp',
  'source/executors/thread_executor.cpp',
  'source/executors/thread_pool_executor.cpp',
  'source/executors/worker_thread_executor.cpp',
  'source/results/impl/consumer_context.cpp',
  'source/results/impl/result_state.cpp',
  'source/results/impl/shared_result_state.cpp',
  'source/results/promises.cpp',
  'source/runtime/runtime.cpp',
  'source/threads/binary_semaphore.cpp',
  'source/threads/thread.cpp',
  'source/timers/timer_queue.cpp',
  'source/timers/timer.cpp',
  'source/task.cpp',
],
include_directories: concurecpp_inc
)

concurencpp_dep = declare_dependency(link_with: concurecpp_lib, include_directories: concurecpp_inc)

subdir('example')