# CHANGELOG: wayland-backend

## Unreleased

## 0.1.0-beta.3

#### Bugfixes

- server-sys: Skip unmanaged globals in the global filter (caused a segfault)

## 0.1.0-beta.2

#### Breaking changes

- server-sys: move `display_ptr()` from `Backend` to `Handle`.

## 0.1.0-beta.1

#### Breaking changes

- Both client and server APIs have been profoundly reworked. The backend now has internal locking
  mechanism allowing handles to it to be cloned and shared accross the application.

#### Bugfixes

- Fix a crash when exactly filling the internal buffers.

## 0.1.0-alpha7

#### Bugfixes

- Client-side with the rust backend, `wl_display` events are now properly printed with other events
  when `WAYLAND_DEBUG=1` is set.

## 0.1.0-alpha6

#### Changes

- Server-side, request callbacks are now allowed to omit providing an `ObjectData` for newly
  created objects if they triggered a protocol error

#### Bugfixes

- Fix display leaks on system server backend.
- Fix a panic when trying to send a message with a null object argument followed by a
  non-null object argument
- Fix various memory leaks

## 0.1.0-alpha5

- Expose `wl_display` pointer on system server backend

## 0.1.0-alpha4

#### Breaking changes

- Server-side `ObjectData::destroyed()` now has access to the `&mut D` server-wide data.

## 0.1.0-alpha3

#### Additions

- Introduce `WEnum::into_result` as a convenience method.

## 0.1.0-alpha2

## 0.1.0-alpha1

Initial pre-release of the crate.