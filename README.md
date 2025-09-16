# vscodeSetup
https://mirrors.ocf.berkeley.edu/gnu/emacs/windows/



;;; path configuracion setup :
;;; C:\Users\dsi\AppData\Roaming/.emacs
(custom-set-variables
 ;; custom-set-variables was added by Custom.
 ;; If you edit it by hand, you could mess it up, so be careful.
 ;; Your init file should contain only one such instance.
 ;; If there is more than one, they won't work right.
 )
(custom-set-faces
;; custom-set-faces was added by Custom.
;; If you edit it by hand, you could mess it up, so be careful.
;; Your init file should contain only one such instance.
;; If there is more than one, they won't work right.
 '(default ((t (:family "Courier New" :foundry "outline" :slant normal :weight regular :height 203 :width normal)))))
;; Desactivar pantalla de inicio
(setq inhibit-startup-message t)

;; Mostrar nÃºmeros de lÃ­nea
(global-display-line-numbers-mode t)
(setq-default indent-tabs-mode t)  ;; usar tab en vez de espacios
(setq-default tab-width 4)         ;; ancho del tab

;; Mostrar parÃ©ntesis emparejados
(show-paren-mode 1)

;; Mejor experiencia con yes/no
(fset 'yes-or-no-p 'y-or-n-p)

;; No dividir lÃ­neas largas, usar scroll horizontal
(setq-default truncate-lines t)

;; Indentar región seleccionada con Ctrl->
(global-set-key (kbd "C-2")
  (lambda () (interactive)
    (indent-rigidly (region-beginning) (region-end) 4)))

;; Desindentar con Ctrl-<
(global-set-key (kbd "C-1")
  (lambda () (interactive)
    (indent-rigidly (region-beginning) (region-end) -4)))

;; Carpeta para paquetes
(require 'package)
(setq package-archives '(("melpa" . "https://melpa.org/packages/")
			 ("gnu" . "https://elpa.gnu.org/packages/")))
(package-initialize)
