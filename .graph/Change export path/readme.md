# Knowledge:
- https://stackoverflow.com/questions/74781015/how-to-convert-the-client-based-file-path-to-the-server-based-when-we-create-sym
>In NFS, symlinks are always resolved by the client. From the perspective of the NFS server, a symlink is just a special type of file but the content (as in, where the symlink points to) is just considered an opaque blob.


# use Symlink
sch: https://www.google.com/search?q=nfs+symlink+export , https://www.google.com/search?q=nfs+symlink+path+instead

## Guide:
- https://access.redhat.com/solutions/8098
This seems to be obsolete, the functionality changed in NFSv4?

## Problem:
- https://community.hpe.com/t5/operating-system-hp-ux/nfs-exporting-symlinks/td-p/3989823

>When I do a showmount -e or exportfs however, it appears that instead of showing /nike1 as exported, the full path is exported -- /export/nike1.
>
>Or is there some way to make the NFS daemon not expand out my symlink to the full "real" path?

## Solution: Use Bind mount instead!