project('cppcoro', ['c', 'cpp'], default_options : ['cpp_std=gnu++2a'])


inc = include_directories('include')
inc_cppcoro = include_directories('include/cppcoro')
inc_detail= include_directories('include/cppcoro/detail')

src = [
  'lib/async_auto_reset_event.cpp',
  'lib/async_manual_reset_event.cpp',
  'lib/async_mutex.cpp',
  'lib/auto_reset_event.cpp',
  'lib/auto_reset_event.hpp',
  'lib/cancellation_registration.cpp',
  'lib/cancellation_source.cpp',
  'lib/cancellation_state.cpp',
  'lib/cancellation_state.hpp',
  'lib/cancellation_token.cpp',
  #'lib/file.cpp',
  #'lib/file_read_operation.cpp',
  #'lib/file_write_operation.cpp',
  'lib/io_service.cpp',
  #'lib/ip_address.cpp',
  #'lib/ip_endpoint.cpp',
  #'lib/ipv4_address.cpp',
  #'lib/ipv4_endpoint.cpp',
  #'lib/ipv6_address.cpp',
  #'lib/ipv6_endpoint.cpp',
  'lib/lightweight_manual_reset_event.cpp',
  #'lib/readable_file.cpp',
  #'lib/read_only_file.cpp',
  #'lib/read_write_file.cpp',
  #'lib/socket_accept_operation.cpp',
  #'lib/socket_connect_operation.cpp',
  #'lib/socket.cpp',
  #'lib/socket_disconnect_operation.cpp',
  'lib/socket_helpers.cpp',
  'lib/socket_helpers.hpp',
  #'lib/socket_recv_from_operation.cpp',
  #'lib/socket_recv_operation.cpp',
  #'lib/socket_send_operation.cpp',
  #'lib/socket_send_to_operation.cpp',
  'lib/spin_mutex.cpp',
  'lib/spin_mutex.hpp',
  'lib/spin_wait.cpp',
  'lib/spin_wait.hpp',
  'lib/static_thread_pool.cpp',
  #'lib/win32.cpp',
  #'lib/writable_file.cpp',
  #'lib/write_only_file.cpp',
]

cppcoro_static = static_library('cppcoro', [src],
                                include_directories: [inc, inc_cppcoro, inc_detail],
                                cpp_args: ['-fcoroutines'],
                                native : true,
                                install: true)

cppcoro_dep = declare_dependency(include_directories: [inc, inc_cppcoro, inc_detail],
                                 compile_args: ['-fcoroutines'],
                                 link_with: cppcoro_static)
