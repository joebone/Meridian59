# Makefile for Delerium's graphics. This makefile doesn't build .bbg files
# but will copy .bgfs from any directory listed here.

TOPDIR=..\..\..
!include $(TOPDIR)\common.mak

SOURCEDIR = .
OUTDIR = $(CLIENTRUNDIR)\resource
OUTDIRSUB = ..\$(OUTDIR)

BGFS = igreyinvis.bgf isitting.bgf itransferitem.bgf iexplosion.bgf irift.bgf \
       minorshard.bgf majorshard.bgf whiteshard.bgf greenshard.bgf \
       purplegemshard.bgf chaosgemshard.bgf greygemshard.bgf \
       rubygemshard.bgf glowgemshard.bgf diamondshard.bgf \
       lightningprismhuge.bgf xaerdun.bgf grd19081.bgf \
       iminorlink.bgf

DIRS = 

all:
   @-for %i in (*.bgf) do @$(CP) %i $(OUTDIR) >nul
   @-for %i in ($(DIRS)) do @if EXIST %i \
      @echo Making in %i & @for %j in (%i\*.bgf) do \
         @$(CP) %j $(OUTDIR) >nul 2>&1

clean:
   @-for %i in (*.bgf) do @if EXIST $(OUTDIR)\%i @del $(OUTDIR)\%i >nul
   @-for %i in ($(DIRS)) do @if EXIST %i \
      @echo Making clean in %i & cd %i & (@for %j in (*.bgf) do \
         @if EXIST $(OUTDIRSUB)\%j @del $(OUTDIRSUB)\%j >nul ) & cd..
